
# Attendance Management using Google Sheets

This project is a simple Login/Logout Attendance Tracker built using:

- 📋 **Google Sheets** for storing data
- 🛠️ **Google Apps Script** as the backend
- 🧩 **HTML + JavaScript** forms for frontend UI

The application allows users to record login and logout times along with location data.

## Project Structure

```
attendance-management/
├── README.md
├── appscript/
│   └── Code.gs
├── forms/
│   ├── basic-form.html
│   └── teacher-attendance-form.html
```

- **appscript/Code.gs** – Google Apps Script backend code
- **forms/basic-form.html** – Basic HTML form
- **forms/teacher-attendance-form.html** – Improved and styled attendance form

## How It Works

### Login:
- Users submit their **Email**, **Name**, **Description**, and **Location**.
- The current **Date** and **Login Time** are automatically recorded in the Google Sheet.

### Logout:
- Users submit their **Email** again.
- The **Logout Time** is recorded in the same row as their login.

### Google Apps Script:
- Handles data writing and updating in the Google Sheet.
- Manages concurrent access using **LockService**.
- Returns JSON responses for success or error messages.

## Setup Instructions

### Google Sheets Setup:
1. Create a new Google Sheet.
2. Add headers like: `Date | Email | Name | Description | Latitude | Longitude | Login | Logout`.

### Apps Script Deployment:
1. Open your Google Sheet.
2. Go to **Extensions > Apps Script**.
3. Paste the content of **appscript/Code.gs** into the editor.
4. Run `initialSetup()` manually once to link the Sheet ID to the script.

### Deploy as a Web App:
1. In the Apps Script editor, go to **Deploy > Manage Deployments > New Deployment**.
2. Select **Web App**.
3. Set the following:
   - **Execute as**: Me
   - **Who has access**: Anyone
4. Deploy the app and copy the **Web App URL**.

### Frontend Forms:
1. Update the `action` attribute inside the HTML forms (`action="..."`) with your Web App deployment URL.
2. Host the HTML files or share them directly with users.

## Technologies Used
- **Google Sheets** – For data storage
- **Google Apps Script** – Backend for processing and storing attendance data
- **HTML5** – Basic structure for forms
- **JavaScript** – Frontend logic
- **LocalStorage** – In teacher form for logout authentication

## Important Notes
- **First-Time Setup**: Don’t forget to run `initialSetup()` manually to link the Google Sheet.
- **Deployment URL**: Ensure your form’s `action` URL points to the correct Web App URL after deployment.
- **Error Handling**: The script will return JSON responses indicating success or error.

## Credits
Developed collaboratively by **[Your Team Name or Member Names]**.

## Screenshots
(Add screenshots of your form here if you want to!)

## License
This project is open-source and free to use. Feel free to contribute, improve, and adapt!
