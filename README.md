# 🩸 Blood Vault - Blood Bank Management System

![Blood Vault](https://img.shields.io/badge/Blood-Vault-red?style=for-the-badge)
![Django](https://img.shields.io/badge/Django-3.0.5-green?style=for-the-badge&logo=django)
![Python](https://img.shields.io/badge/Python-3.7+-blue?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

> **A modern, efficient blood bank management system to save lives through seamless blood donation and request management.**

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Technology Stack](#-technology-stack)
- [Screenshots](#-screenshots)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [Usage Guide](#-usage-guide)
  - [Admin](#admin)
  - [Donor](#donor)
  - [Patient](#patient)
- [Project Structure](#-project-structure)
- [Database Schema](#-database-schema)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)
- [Acknowledgments](#-acknowledgments)

---

## 🌟 About the Project

**Blood Vault** is a comprehensive blood bank management system designed to bridge the gap between blood donors and patients in need. The system facilitates:

- 🩸 **Blood Donation Management**: Streamlined process for donors to register and donate blood
- 🏥 **Blood Request Processing**: Quick and efficient blood request handling for patients
- 📊 **Inventory Tracking**: Real-time blood stock monitoring across all blood groups
- ✅ **Approval Workflow**: Admin-controlled approval system for donations and requests
- 📈 **Dashboard Analytics**: Comprehensive statistics and tracking for all user roles

### 🎯 Mission
To save lives by making blood donation and requests more accessible, efficient, and transparent.

---

## ✨ Features

### 🔐 Admin Portal
- **Dashboard Analytics**
  - Real-time blood stock levels for all blood groups (A+, A-, B+, B-, AB+, AB-, O+, O-)
  - Total donor count
  - Blood request statistics (Total, Approved, Pending, Rejected)
  - Total blood units available

- **Donor Management**
  - View all registered donors
  - Update donor information
  - Delete donor accounts
  - Track donor history

- **Patient Management**
  - View all registered patients
  - Update patient information
  - Delete patient accounts
  - Monitor patient requests

- **Donation Management**
  - Review blood donation requests
  - Approve/Reject donations with disease screening
  - Automatic blood stock updates on approval
  - Donation history tracking

- **Request Management**
  - Process blood requests from donors and patients
  - Approve/Reject based on stock availability
  - Automatic stock deduction on approval
  - Request history with status tracking

- **Blood Stock Control**
  - Manual adjustment of blood group units
  - Real-time inventory updates
  - Stock availability checks

### 🩸 Donor Portal
- **Easy Registration**
  - Simple sign-up process with basic details
  - Blood group selection
  - Profile picture upload

- **Blood Donation**
  - Submit donation requests
  - Specify blood group and units
  - Track donation status (Pending, Approved, Rejected)

- **Blood Request**
  - Donors can also request blood if needed
  - Request specific blood groups and units
  - View request history

- **Personal Dashboard**
  - Total requests made
  - Approved requests count
  - Pending requests count
  - Rejected requests count
  - Complete donation and request history

### 🏥 Patient Portal
- **Quick Registration**
  - No approval required - instant access
  - Simple registration form
  - Blood group selection

- **Blood Request**
  - Request specific blood group and units
  - Provide reason for request
  - Patient details (name, age)

- **Request Tracking**
  - View all blood requests
  - Real-time status updates
  - Request history with timestamps

- **Personal Dashboard**
  - Total requests made
  - Approved requests
  - Pending requests
  - Rejected requests

---

## 🛠️ Technology Stack

### Backend
- **Framework**: Django 3.0.5
- **Language**: Python 3.7+
- **Database**: SQLite (Development) / PostgreSQL (Production Ready)

### Frontend
- **HTML5** - Structure
- **CSS3** - Styling with custom design
- **JavaScript** - Interactivity
- **Bootstrap 4.3.1** - Responsive layout
- **Font Awesome 5.14.0** - Icons

### Additional Libraries
- **django-widget-tweaks** - Enhanced form rendering
- **asgiref** - ASGI server
- **sqlparse** - SQL parsing
- **pytz** - Timezone support

---

## 📸 Screenshots

### Homepage
![Homepage](static/screenshot/homepage.png)
*Clean, modern landing page with call-to-action buttons*

### Admin Dashboard
![Admin Dashboard](static/screenshot/admindashboard.png)
*Comprehensive overview of blood inventory and statistics*

### Blood Donation
![Blood Donation](static/screenshot/blooddonation.png)
*Donor portal for blood donation requests*

### Blood Request
![Blood Request](static/screenshot/bloodrequest.png)
*Patient portal for blood requests*

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Python 3.7 or higher**
  ```bash
  python --version
  ```

- **pip** (Python package manager)
  ```bash
  pip --version
  ```

- **Git** (for cloning the repository)
  ```bash
  git --version
  ```

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/sunnyy-14/Blood_Vault.git
   cd Blood_Vault
   ```

2. **Navigate to Project Directory**
   ```bash
   cd bloodbankmanagement
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or if you prefer using Python module:
   ```bash
   python -m pip install -r requirements.txt
   ```

4. **Apply Database Migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create Superuser (Admin Account)**
   ```bash
   python manage.py createsuperuser
   ```
   
   You'll be prompted to enter:
   - Username
   - Email address (optional)
   - Password (type carefully - it won't be visible)
   - Password confirmation

6. **Collect Static Files** (Optional - for production)
   ```bash
   python manage.py collectstatic
   ```

### Running the Application

1. **Start the Development Server**
   ```bash
   python manage.py runserver
   ```

2. **Access the Application**
   
   Open your web browser and navigate to:
   ```
   http://127.0.0.1:8000/
   ```

3. **Login Portals**
   - **Admin**: `http://127.0.0.1:8000/adminlogin`
   - **Donor**: `http://127.0.0.1:8000/donor/donorlogin`
   - **Patient**: `http://127.0.0.1:8000/patient/patientlogin`

4. **Stop the Server**
   
   Press `Ctrl + C` in the terminal

---

## 📖 Usage Guide

### Admin

1. **Initial Setup**
   - Login with superuser credentials at `/adminlogin`
   - The system automatically creates blood group entries (A+, A-, B+, B-, AB+, AB-, O+, O-)
   - Update initial blood stock units

2. **Managing Donations**
   - Navigate to "Donation" from admin menu
   - Review pending donation requests
   - Check donor's disease information
   - Approve (adds units to stock) or Reject (no stock change)

3. **Processing Requests**
   - Go to "Blood Request" section
   - View pending requests with patient/donor details
   - Check stock availability
   - Approve if sufficient stock (auto-deducts units)
   - Reject if insufficient stock

4. **Updating Stock**
   - Access "Blood" section
   - Select blood group
   - Enter new unit count
   - Submit to update

### Donor

1. **Registration**
   - Click "Donate Now" on homepage
   - Fill registration form (name, email, blood group, etc.)
   - Upload profile picture
   - Submit and login

2. **Donating Blood**
   - Login to donor portal
   - Click "Donate Blood"
   - Fill donation form (units, disease information)
   - Submit for admin approval
   - Track status in "Donation History"

3. **Requesting Blood**
   - Navigate to "Make Request"
   - Fill request form (patient name, age, reason, blood group, units)
   - Submit request
   - Monitor status in "Request History"

### Patient

1. **Registration**
   - Click "Need Blood" on homepage
   - Complete registration form
   - Login immediately (no approval needed)

2. **Requesting Blood**
   - Login to patient portal
   - Go to "Make Request"
   - Provide patient details and requirements
   - Submit request
   - Check "My Requests" for status updates

---

## 📁 Project Structure

```
Blood_Vault/
│
├── bloodbankmanagement/          # Main project directory
│   ├── blood/                    # Blood management app
│   │   ├── migrations/           # Database migrations
│   │   ├── templates/            # HTML templates
│   │   ├── admin.py              # Admin configurations
│   │   ├── forms.py              # Form definitions
│   │   ├── models.py             # Database models (Stock, BloodRequest)
│   │   ├── views.py              # View functions
│   │   └── urls.py               # URL routing
│   │
│   ├── donor/                    # Donor management app
│   │   ├── migrations/
│   │   ├── templates/
│   │   ├── models.py             # Donor, BloodDonate models
│   │   ├── views.py              # Donor portal views
│   │   └── forms.py              # Donor forms
│   │
│   ├── patient/                  # Patient management app
│   │   ├── migrations/
│   │   ├── templates/
│   │   ├── models.py             # Patient model
│   │   ├── views.py              # Patient portal views
│   │   └── forms.py              # Patient forms
│   │
│   ├── bloodbankmanagement/      # Project settings
│   │   ├── settings.py           # Django settings
│   │   ├── urls.py               # Main URL configuration
│   │   └── wsgi.py               # WSGI configuration
│   │
│   ├── static/                   # Static files
│   │   ├── css/                  # Stylesheets
│   │   ├── image/                # Images
│   │   ├── profile_pic/          # Uploaded profile pictures
│   │   └── screenshot/           # Application screenshots
│   │
│   ├── templates/                # Global templates
│   │   ├── blood/                # Blood app templates
│   │   ├── donor/                # Donor app templates
│   │   └── patient/              # Patient app templates
│   │
│   ├── manage.py                 # Django management script
│   ├── requirements.txt          # Python dependencies
│   └── db.sqlite3                # SQLite database (dev)
│
├── SETUP_GUIDE.md                # Detailed setup instructions
├── README.md                     # This file
└── .gitignore                    # Git ignore rules
```

---

## 🗄️ Database Schema

### Models

#### **Stock** (blood.models)
- `bloodgroup`: CharField - Blood group type (A+, A-, etc.)
- `unit`: PositiveIntegerField - Available units (default: 0)

#### **BloodRequest** (blood.models)
- `request_by_patient`: ForeignKey - Patient who requested (nullable)
- `request_by_donor`: ForeignKey - Donor who requested (nullable)
- `patient_name`: CharField - Name of patient
- `patient_age`: PositiveIntegerField - Age of patient
- `reason`: CharField - Reason for blood request
- `bloodgroup`: CharField - Required blood group
- `unit`: PositiveIntegerField - Units requested
- `status`: CharField - Status (Pending/Approved/Rejected)
- `date`: DateField - Request date (auto)

#### **Donor** (donor.models)
- `user`: OneToOneField - Linked User account
- `bloodgroup`: CharField - Donor's blood group
- `age`: PositiveIntegerField - Donor's age
- `mobile`: CharField - Contact number
- `address`: CharField - Donor's address
- `profile_pic`: ImageField - Profile picture

#### **BloodDonate** (donor.models)
- `donor`: ForeignKey - Donor making donation
- `bloodgroup`: CharField - Blood group to donate
- `unit`: PositiveIntegerField - Units to donate
- `disease`: CharField - Medical history/diseases
- `status`: CharField - Status (Pending/Approved/Rejected)
- `date`: DateField - Donation date (auto)

#### **Patient** (patient.models)
- `user`: OneToOneField - Linked User account
- `bloodgroup`: CharField - Patient's blood group
- `age`: PositiveIntegerField - Patient's age
- `mobile`: CharField - Contact number
- `address`: CharField - Patient's address
- `profile_pic`: ImageField - Profile picture

---

## 🔧 Configuration

### Settings

Key configurations in `bloodbankmanagement/settings.py`:

```python
# Database Configuration
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

# Static Files
STATIC_URL = '/static/'
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]

# Media Files
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

# Allowed Hosts (Update for production)
ALLOWED_HOSTS = ['127.0.0.1', 'localhost']
```

---

## 🚢 Deployment

### Production Checklist

- [ ] Set `DEBUG = False` in settings.py
- [ ] Configure `ALLOWED_HOSTS`
- [ ] Use PostgreSQL or MySQL instead of SQLite
- [ ] Set up environment variables for secrets
- [ ] Configure static files serving (WhiteNoise/Nginx)
- [ ] Set up SSL certificate (HTTPS)
- [ ] Configure email backend for notifications
- [ ] Set up backup strategy for database
- [ ] Configure logging
- [ ] Set up monitoring (Sentry, etc.)

### Deployment Platforms

**Recommended platforms:**
- **Heroku** - Easy deployment with Git
- **PythonAnywhere** - Simple Django hosting
- **AWS EC2** - Full control and scalability
- **DigitalOcean** - Balance of simplicity and control
- **Railway** - Modern deployment platform

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

### How to Contribute

1. **Fork the Project**
2. **Create your Feature Branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your Changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the Branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Contribution Guidelines

- Follow PEP 8 style guide for Python code
- Write meaningful commit messages
- Update documentation for new features
- Add tests for new functionality
- Ensure all tests pass before submitting PR

---

## 📝 License

Distributed under the MIT License. See `LICENSE` file for more information.

---

## 📧 Contact

**Project Maintainer**: Sunny

**Email**: sunnyverma1405@gmail.com

**Project Link**: [https://github.com/YOUR_USERNAME/Blood_Vault](https://github.com/YOUR_USERNAME/Blood_Vault)

---

## 🙏 Acknowledgments

### Original Developer
- **Sumit Kumar** - Original blood bank management system
- [Facebook](https://fb.com/sumit.luv)
- [YouTube - LazyCoder](https://youtube.com/lazycoders)

### Technologies Used
- [Django](https://www.djangoproject.com/) - Web framework
- [Bootstrap](https://getbootstrap.com/) - UI framework
- [Font Awesome](https://fontawesome.com/) - Icons
- [Python](https://www.python.org/) - Programming language

### Resources
- Django Documentation
- Stack Overflow Community
- GitHub Community

---

## 🔮 Future Enhancements

- [ ] Email notifications for request status updates
- [ ] SMS alerts for critical blood shortage
- [ ] Blood donation camps management
- [ ] Certificate generation for donors
- [ ] Advanced analytics and reporting
- [ ] Mobile application (React Native)
- [ ] API for third-party integrations
- [ ] Multi-language support
- [ ] Geolocation-based donor search
- [ ] Blood donation appointment scheduling
- [ ] Integration with hospital management systems
- [ ] Donor rewards and recognition system
- [ ] Emergency blood request alerts

---

## 📊 Project Statistics

- **Total Lines of Code**: ~5000+
- **Languages**: Python, HTML, CSS, JavaScript
- **Dependencies**: 5 main packages
- **Database Tables**: 5 main models
- **User Roles**: 3 (Admin, Donor, Patient)
- **Blood Groups Supported**: 8 (A+, A-, B+, B-, AB+, AB-, O+, O-)

---

## 🐛 Known Issues

- [ ] Profile picture preview before upload
- [ ] Email verification for new registrations
- [ ] Password reset functionality
- [ ] Export data to CSV/PDF

*Report issues at: [GitHub Issues](https://github.com/YOUR_USERNAME/Blood_Vault/issues)*

---

## ❓ FAQ

**Q: Can donors request blood too?**  
A: Yes! Donors can both donate and request blood through their portal.

**Q: How are blood stock units managed?**  
A: Admin can manually update stock levels, and the system automatically adjusts units when donations are approved (+units) or requests are fulfilled (-units).

**Q: What happens if a request is rejected?**  
A: Rejected requests don't affect blood stock. The status is simply updated to "Rejected" and the requester is notified via their dashboard.

**Q: Is there a limit on blood units that can be requested?**  
A: No system limit, but admin can reject requests that exceed available stock.

**Q: Can I use this for production?**  
A: Yes, but please follow the production checklist and security best practices.

---

<div align="center">

### ⭐ Star this repository if you found it helpful!

**Made with ❤️ and 🩸 to save lives**

![Blood Vault](https://img.shields.io/badge/Blood-Vault-red?style=for-the-badge)

*Every drop counts. Every donor matters.*

</div>

---

© 2026 Blood Vault. All rights reserved.
