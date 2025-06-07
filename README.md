# File Sharer Documentation

## Introduction

File Sharer is a secure and stylish web-based application that allows users to upload, download, and manage files and folders seamlessly. Developed using Streamlit, this app enables encrypted file uploads, individual and batch downloads, and special developer functions with a built-in command prompt. Whether for personal file access or group sharing in a local or deployed environment, File Sharer simplifies secure file transfer with a sleek UI.

---

## Features

### 🔐 Secure Uploads

* Users can upload individual files or folders.
* Optional password protection ensures file privacy.

### 📥 Easy Downloads

* Users can download files or zipped folders directly from the app.
* Developer users can delete files.

### 🧠 Intelligent UI

* Splash screen with animated title.
* Responsive download/delete buttons with CSS glow effects.
* Command prompt available for hidden features and developer controls.

### 🧙 Developer Mode

* Unlockable using secret commands.
* Allows deletion of files and access to advanced options.

### 💼 Persistent Storage

* Files and folders persist across sessions until explicitly deleted or app restart.

### 🗂 Folder Handling

* Multiple file uploads zipped into a single downloadable `.zip` file.

---

## Requirements

* Python 3.8+
* `streamlit`
* `hashlib`, `base64`, `json`, `os`, `shutil`, `io`, `zipfile`, `time`

Install dependencies using:

```bash
pip install streamlit
```

---

## File Structure

```
📁 File Sharer
│
├── app.py                  # Main application file
├── uploaded_files/         # Uploaded files & folders saved here
├── file_metadata.json      # Password hash and metadata storage
```

---

## Developer Mode

To unlock special controls like deleting files:

1. Click "Command Prompt"
2. Enter secret command like: `override protocol-amphibiar`

Developer mode enables:

* Deleting files and folders
* Executing internal commands (e.g., `downloadall`, `exit dev mode`)

---

## Security

* Passwords are stored using SHA-256 hashes.
* Only the correct password grants access to protected files.
* Developer access can only be unlocked through specific commands.

---

## Styling and UX

* Animated typewriter splash screen
* Responsive and modern buttons
* Glow animation and custom font colors for terminal aesthetics
* Toggle developer mode without page reloads

---

## Future Enhancements

* File sharing via URL
* Cloud integration (Google Drive, Dropbox)
* Login system with user-based access
* File expiration and auto-deletion features

---

## Developer

Developed by Amphibiar
