# PayU Payment Integration Module for Odoo

This is a custom **Odoo** module written in **Python** that integrates the **PayU** payment gateway with the Odoo platform.  
It enables merchants to configure PayU credentials, process customer payments, and manage transactions — all within the Odoo backend.

> 📚 Need help setting up Odoo before using this module?  
> 👉 Follow this step-by-step guide:  
> **[How to Install Odoo on Your Server or Local Machine](https://www.odiware.com/odoo/how-to-install-odoo-on-your-server-or-local-machine/)**

```

## 📁 Project Structure
payu_payments_for_odoo/
│
├── const.py # Constants used across the module
├── init.py # Module initializer
├── manifest.py # Metadata and dependencies
│
├── controllers/ # HTTP controllers for frontend/API routes
│ ├── main.py
│ └── init.py
│
├── data/
│ └── payment_provider_data.xml # Initial PayU provider records
│
├── models/ # Business logic and model extensions
│ ├── payment_provider.py
│ ├── payment_transaction.py
│ └── init.py
│
├── static/description/ # Icons for the Odoo app view
│ ├── icon.png
│ └── icon.svg
│
├── views/ # XML views and UI customizations
│ ├── payment_payu_templates.xml
│ └── payment_provider_views.xml
│
└── pycache/ # Auto-generated Python bytecode

```

## ⚙️ Features

- Configure PayU credentials (Key/Salt)
- Redirect customers to PayU for secure payment processing
- Handle validation, confirmation, and error states
- Integrate seamlessly with Odoo’s native payment flow
- Support fixed discounts and dynamic invoice amount due updates
- Cleanly separated controllers, models, and views

---

## 🛠 Requirements

- **Odoo 18**
- **Python 3.11 or 3.12**
- **Valid PayU merchant account**

---

## 🚀 Installation & Usage

1. **Clone or copy** this module into your Odoo custom addons directory:  
   Example:  
   `C:\Odoo\custom-addons\payu_payments_for_odoo`

2. **Update your `odoo.conf`** file to include the custom addons path:

   ```ini
   [options]
   addons_path = C:\Program Files\Odoo 18.0\server\odoo\addons,C:\Odoo\custom-addons
## 🔁 Setup Instructions for PayU Payment Provider in Odoo

### 1. Restart the Odoo Server
Make sure to restart your Odoo instance to load the new module.

---

### 2. Activate Developer Mode
In the Odoo interface:

- Click on your profile menu (top-right)
- Select **"Activate Developer Mode"**

---

### 3. Install the PayU Module

- Go to **Apps**
- Click **Update App List**
- Search for **PayU Payment Provider**
- Click **Install**

> ⚠️ Ensure the **Website** module is also installed — it's required for the checkout/payment flow.

---

### 4. Configure PayU Provider

- Go to **Configuration → Payment Providers → PayU**
- Enter your **Key** and **Salt**  
  or use the **Sign up** option to create a new PayU account
- **Enable** the provider

---

### ✅ You're all set!
You can now accept **PayU payments** directly through Odoo!
