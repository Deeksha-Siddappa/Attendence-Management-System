🗂️ Attendance Management using Google Sheets
This project is a simple Login/Logout Attendance Tracker built using:

📋 Google Sheets (for storing data)

🛠️ Google Apps Script (as the backend)

🧩 HTML + JavaScript forms (frontend UI)

It allows users to record login and logout times along with location data.

📜 Project Structure
css
Copy
Edit
attendance-management/
├── README.md
├── appscript/
│   └── Code.gs
├── forms/
│   ├── basic-form.html
│   └── teacher-attendance-form.html
appscript/Code.gs – Google Apps Script backend code

forms/basic-form.html – Basic HTML form

forms/teacher-attendance-form.html – Improved and styled attendance form

⚙️ How It Works
Login:

Users submit their Email, Name, Description, and Location.

The current Date and Login Time are automatically recorded.

Logout:

Users submit their Email again.

The Logout Time is recorded in the same row as their login.

Google Apps Script:

Handles data writing and updating in the sheet.

Manages concurrent access using LockService.

Returns JSON responses.

🚀 Setup Instructions
Google Sheets Setup:

Create a new Google Sheet.

Add headers like: Date | Email | Name | Description | Latitude | Longitude | Login | Logout.

Apps Script Deployment:

Open Extensions > Apps Script from the Sheet.

Paste the content of appscript/Code.gs.

Run initialSetup() manually once to link the Sheet ID.

Deploy as a Web App:

Execute as: Me

Access: Anyone

Frontend Forms:

Update the action URL inside your HTML forms (action="...") with your Web App deployment URL.

Host the HTML files or share them directly.

🛠️ Technologies Used
Google Sheets

Google Apps Script

HTML5

JavaScript

LocalStorage (in teacher form for logout authentication)

📌 Important Notes
First-Time Setup: Don't forget to run initialSetup() manually!

Deployment URL: Make sure your form points to the correct Web App URL after you deploy.

Error Handling: The script returns JSON success or error messages.

✨ Credits
Developed collaboratively by [Your Team Name or Member Names]

📸 Screenshots
(You can add screenshots of your form here later if you want!)

📢 License
This project is open-source and free to use.
Feel free to contribute, improve, and adapt!

✅ To-Do (Optional)
 Add email notifications.

 Improve UI/UX further.

 Add QR code scanning for faster login/logout.