# Algol - Automatic Email Scheduler

Algol is an advanced email automation tool built using **Express.js** and **React**, designed to help you schedule and automate your email campaigns with ease. Whether you need to send recurring emails, schedule one-time messages, or track your email history, Algol provides a seamless experience for managing your email communications.

---

## Features

- **User Authentication**: 
  - Sign up and log in using your email or **Google OAuth** for a secure and hassle-free experience.
  
- **Email Configuration**: 
  - Set up the email address from which your scheduled messages will be sent. Currently supports **Gmail** only.

- **Bulk Emails**: 
  - Send emails to multiple recipients with **CC** and **BCC** support.

- **Scheduling Options**: 
  - Automate your emails by scheduling them on a **Daily**, **Weekly**, **Monthly**, or **Yearly** basis.
  - Set up **recurring emails** at intervals of **20/30 seconds** or **minutes**.

- **Email Tracking**: 
  - Track all **active** and **past emails** in the **History** section.
  - View detailed logs of sent emails, including timestamps and recipient lists.

- **Customizable Email Templates**: 
  - Create and save email templates for quick reuse.
  - Personalize emails with dynamic placeholders for recipient names and other details.

- **User-Friendly Dashboard**: 
  - Intuitive interface for managing scheduled emails, templates, and history.

---

## Known Issues

- **Gmail Limitation**: 
  - Currently, the service is limited to **Gmail accounts only**. Support for other email providers (e.g., Outlook, Yahoo) is under development.

- **Insecure Connection**: 
  - Hosting on a server with an insecure connection may raise **CSP (Content Security Policy)** issues.
  - **Workaround**: Change your browser settings or build the app locally.

- **Recurring Email Limits**: 
  - Due to Gmail's sending limits, recurring emails with very short intervals (e.g., every 20 seconds) may hit rate limits.

---

## Getting Started

Follow these steps to set up Algol on your local machine.

### Prerequisites

- **Node.js** (v16 or higher) and **npm** installed on your machine.
- A **MongoDB Atlas** account or a local MongoDB instance.
- A **Gmail account** for sending emails (ensure you have enabled **less secure apps** or set up an **App Password**).

---

### Step-by-Step Installation Guide

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-repo/algol-email-scheduler.git
   cd algol-email-scheduler
   ```

2. **Install Dependencies**

   Install all the necessary dependencies using npm.

   ```bash
   npm install
   ```

3. **Set Up MongoDB**

   - Create a **MongoDB cluster** using [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) or set up a local MongoDB instance.
   - Whitelist your IP address in the MongoDB Atlas cluster settings if you're using Atlas.

4. **Configure Environment Variables**

   Create a `.env` file in the root directory of the project and add the following environment variables:

   ```env
   DB_URI=<your-mongodb-connection-string>
   DB_NS=<your-database-name>
   PORT=5000
   GOOGLE_CLIENT_ID=<your-google-client-id>
   GOOGLE_CLIENT_SECRET=<your-google-client-secret>
   GMAIL_USER=<your-gmail-address>
   GMAIL_PASSWORD=<your-gmail-app-password>
   ```

   Replace the placeholders with your actual credentials:
   - `<your-mongodb-connection-string>`: Your MongoDB connection URI.
   - `<your-database-name>`: Your desired database name.
   - `<your-google-client-id>` and `<your-google-client-secret>`: Google OAuth credentials (create these in the [Google Cloud Console](https://console.cloud.google.com/)).
   - `<your-gmail-address>`: The Gmail address you want to use for sending emails.
   - `<your-gmail-app-password>`: Your Gmail App Password (generate this in your Google Account settings).

5. **Start the Server**

   To start the server, run the following command:

   ```bash
   npm start
   ```

   The server will start running on `http://localhost:5000`.

6. **Run the Development Server**

   If you plan to make changes to the React files, start the development server using:

   ```bash
   npm run dev
   ```

7. **Access the Application**

   Open your browser and navigate to `http://localhost:5000` to access Algol.

---

## Usage

### 1. **Sign Up / Log In**
   - Use your email or Google account to sign up or log in.

### 2. **Configure Your Email**
   - Go to the **Settings** page and configure the email address you want to use for sending scheduled emails.

### 3. **Create a Scheduled Email**
   - Navigate to the **Compose** page.
   - Enter the recipient(s), subject, and body of the email.
   - Choose the scheduling options (e.g., Daily, Weekly, Recurring).
   - Click **Schedule** to set up the email.

### 4. **Track Your Emails**
   - View all active and past emails in the **History** section.
   - Check the status of each email (e.g., Sent, Pending, Failed).

### 5. **Manage Templates**
   - Create and save email templates for quick reuse.
   - Edit or delete templates as needed.

---

## Contributing

We welcome contributions from the community! If you'd like to contribute, please check out the [Issues](https://github.com/your-repo/algol-email-scheduler/issues) section for a list of features we're working on and those that are needed. Feel free to fork the repository, make your changes, and submit a pull request.

### How to Contribute:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes and test them thoroughly.
4. Submit a pull request with a detailed description of your changes.

---

## Roadmap

Here are some planned features for future releases:
- **Support for Multiple Email Providers**: Add support for Outlook, Yahoo, and other email services.
- **Advanced Analytics**: Provide detailed analytics on email open rates, click-through rates, and more.
- **Team Collaboration**: Allow multiple users to manage and schedule emails from a shared account.
- **Email Templates Marketplace**: Allow users to share and download email templates.

---

## Support

If you encounter any issues or have questions, please open an issue on the [GitHub repository](https://github.com/your-repo/algol-email-scheduler/issues). For additional support, you can reach out to us at **support@algol.com**.

---

<h1 align="center">
   Thanks for visiting Algol!
</h1>

<p align="center">
   <em>Automate your emails, save time, and focus on what matters most.</em>
</p>
