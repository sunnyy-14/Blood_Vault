# Blood Vault - Setup Guide

## 🩸 Blood Bank Management System

This is a Django-based blood bank management system with three user roles: Admin, Donor, and Patient.

---

## 📋 Prerequisites

Before starting, make sure you have:
- **Python 3.7 or higher** installed
- **pip** (Python package manager)
- **Git** installed

---

## 🚀 Setup Instructions

### Step 1: Clone the Repository
Open a terminal and run:
```bash
git clone https://github.com/sunnyy-14/Blood_Vault.git
cd Blood_Vault/bloodbankmanagement
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Setup Database
Run these commands one by one:

```bash
python manage.py makemigrations
```

```bash
python manage.py migrate
```

### Step 4: Create Admin Account
```bash
python manage.py createsuperuser
```

You'll be asked to provide:
- **Username**: (choose any username)
- **Email**: (optional, can skip by pressing Enter)
- **Password**: (type carefully, won't be visible)
- **Password confirmation**: (type again)

### Step 5: Run the Server
```bash
python manage.py runserver
```

### Step 6: Open in Browser
Open your browser and go to:
```
http://127.0.0.1:8000/
```

---

## 👥 User Roles & Features

### 🔑 Admin
- Login at: `http://127.0.0.1:8000/adminlogin`
- **Dashboard**: View blood stock, donor count, request statistics
- **Manage Donors**: View, update, delete donor accounts
- **Manage Patients**: View, update, delete patient accounts
- **Approve/Reject Donations**: Review blood donation requests
- **Approve/Reject Blood Requests**: Manage blood request from donors/patients
- **Update Blood Stock**: Manually adjust blood units per group

### 🩸 Donor
- **Sign Up**: Create account with basic details
- **Donate Blood**: Submit donation requests (requires admin approval)
- **Request Blood**: Can also request blood if needed
- **View History**: See donation and request history with status
- **Dashboard**: Track requests (Made, Approved, Pending, Rejected)

### 🏥 Patient
- **Sign Up**: Create account (no approval needed)
- **Request Blood**: Request specific blood group and units
- **View History**: See blood request history with status
- **Dashboard**: Track requests (Made, Approved, Pending, Rejected)

---

## 🛠️ Tech Stack

- **Backend**: Django 3.0.5 (Python web framework)
- **Database**: SQLite (default, built into Django)
- **Frontend**: HTML, CSS, JavaScript
- **UI Components**: django-widget-tweaks

---

## 📁 Project Structure

```
Blood_Vault/
└── bloodbankmanagement/
    ├── blood/              # Blood management app
    ├── donor/              # Donor management app
    ├── patient/            # Patient management app
    ├── bloodbankmanagement/  # Main project settings
    ├── static/             # CSS, JS, images
    ├── templates/          # HTML templates
    ├── manage.py           # Django management script
    └── requirements.txt    # Python dependencies
```

---

## 🐛 Troubleshooting

### Issue: "python is not recognized"
- Make sure Python is installed and added to PATH
- Try using `py` instead of `python`

### Issue: Port already in use
- Stop the server with `Ctrl + C`
- Use a different port: `python manage.py runserver 8080`

### Issue: Module not found
- Reinstall dependencies: `pip install -r requirements.txt`

### Issue: Database errors
- Delete `db.sqlite3` file
- Run migrations again:
  ```bash
  python manage.py makemigrations
  python manage.py migrate
  ```

---

## 📞 Next Steps

1. ✅ Follow the setup instructions above
2. 🔐 Create your admin account
3. 🌐 Open the application in browser
4. 🎨 Explore the interface
5. 🛠️ Let me know if you need any customizations!

---

## 💡 Need Help?

If you face any issues during setup, just let me know and I'll help you troubleshoot!

---

**Project**: Blood Vault System
