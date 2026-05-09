# MediCare Clinic - Appointment Booking System

A simple clinic appointment booking system with a patient booking form and doctor dashboard.

## Quick Start (⚠️ Important!)

Follow these steps **exactly** on your laptop:

### 1. Install Node.js
- Download and install from: https://nodejs.org/
- Verify installation by opening Terminal/Command Prompt and typing: `node --version`

### 2. Open Terminal in Project Folder
- Go to the folder containing these files
- Right-click → Open Command Prompt/Terminal here (or use `cd` command)

### 3. Install Dependencies
```bash
npm install
```
This downloads `express` and `cors` (required libraries).

### 4. Start the Server
```bash
npm start
```
or simply:
```bash
node server.js
```

You should see: ✅ MediCare backend running at http://localhost:4000

### 5. Run as Desktop App
```bash
npm run desktop
```

This opens MediCare in a desktop window using Electron.

### 6. Open in Browser
- **On the same laptop:** Go to: http://localhost:4000
- **From another laptop on same WiFi:** Go to: http://192.168.1.108:4000
  - (Replace `192.168.1.108` with your server's IP address)
- Done! 🎉

---

## Accessing from Another Laptop (Network Setup)

### If you're running the server on Laptop A and want to access from Laptop B:

1. **Find your server's IP address:**
   - Windows: Open Command Prompt and type `ipconfig` → Look for "IPv4 Address"
   - Mac/Linux: Open Terminal and type `ifconfig` or `hostname -I`
   - It will look like: `192.168.x.x`

2. **On the other laptop:**
   - Open browser and go to: `http://[SERVER-IP]:4000`
   - Example: `http://192.168.1.108:4000`

3. **Both laptops must be on the same WiFi network!**

---

## Features

### 👤 Patient Booking
- Fill appointment form with personal details
- Select preferred date and time
- Choose reason for visit
- Form validation included

### 🔐 Doctor Dashboard
- Secure login (see credentials below)
- View all appointments
- Filter by status (pending/confirmed/cancelled)
- Approve or cancel appointments

### Default Doctor Credentials
- **Username:** `harshith`
- **Password:** `123`

---

## Files Explained

| File | Purpose |
|------|---------|
| `index.html` | Frontend - patient form + doctor dashboard |
| `server.js` | Backend - API endpoints + data storage |
| `package.json` | Project dependencies |
| `appointments.json` | Database (created automatically) |

---

## Troubleshooting

### ❌ "command not found: npm"
→ Node.js not installed. Download from https://nodejs.org/

### ❌ "Cannot find module 'express'"
→ Run: `npm install` in the project folder

### ❌ "Port 4000 already in use"
→ Close other apps using port 4000, or edit `const PORT = 4000;` in `server.js`

### ❌ Page shows "Cannot reach server"
**On same laptop?** Make sure `npm start` is running
**On another laptop?** 
→ Check both laptops are on same WiFi
→ Replace `192.168.1.108` with the actual server IP address

### ❌ Cannot access from another laptop
1. Open Command Prompt on the server laptop
2. Type `ipconfig` and find your IPv4 address
3. Tell the other person to use: `http://[YOUR-IP]:4000`
4. Make sure Windows Firewall isn't blocking port 4000

---

## Notes
- This is a local project (runs on your computer only)
- Appointments are saved in `appointments.json`
- No internet connection needed (works on local WiFi)
- Server must be running for the app to work
- IP address may change if WiFi restarts (update accordingly)
