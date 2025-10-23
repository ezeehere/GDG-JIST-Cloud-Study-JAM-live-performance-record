# GDG JIST Cloud Study Jam Dashboard

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)

A dynamic, client-side dashboard to track participant progress for the **GDG on Campus JIST Cloud Study Jam**.

This project was built to gamify the event, provide real-time stats to organizers, and motivate participants by showing community progress towards swag tiers. It's built with pure HTML, Tailwind CSS, and JavaScript, and it fetches live data from a public Google Sheet, making it lightweight and easy to deploy.

**Demo Screenshot:**
[https://i.ibb.co/35z0bnpc/Untitled.png]

## ✨ Features

* 📈 **Real-time Statistics:** Summary cards show total participants, redeemed codes, eligible participants, and total swag earners.
* 🏆 **Top 3 Leaderboard:** Automatically displays the top 3 participants based on the number of skill badges completed.
* 📊 **Searchable Participant Table:** A complete table of all participants, searchable by name or email.
* 🔍 **Quick Filters:** Click on the summary cards (e.g., "Ineligible", "Eligible for Swags") to instantly filter the main table.
* 🎁 **Community Swag Tracker:** A dedicated "Swags" page with an animated progress bar showing community progress towards unlocking different swag tiers.
* 🖱️ **Participant Detail Modal:** Click "View Details" on any participant to see their list of completed skill badges and arcade games.
* ⏳ **Draggable Countdown:** A persistent, draggable timer counts down to the event's completion deadline.
* 📱 **Fully Responsive:** Built with Tailwind CSS, the layout adapts perfectly to desktop and mobile devices.
* 🚀 **Zero Backend:** Uses [PapaParse](https://www.papaparse.com/) to parse a live CSV from Google Sheets directly in the browser.

## 🛠️ Tech Stack

* **Frontend:** HTML5, [Tailwind CSS](https://tailwindcss.com/)
* **JavaScript:** Vanilla JavaScript (ES6+), [PapaParse](https://www.papaparse.com/)
* **Data Source:** [Google Sheets](https://www.google.com/sheets/about/)

## 🚀 How to Use / Setup

This is a static website. You can run it by simply opening the `index.html` file, but the most important step is to link your own Google Sheet.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Publish Your Google Sheet to the Web:**
    * Open your Google Sheet containing the participant data.
    * Go to `File` > `Share` > `Publish to web`.
    * In the `Link` tab, select the specific sheet (e.g., `Sheet1`) you want to publish.
    * In the dropdown, select `Comma-separated values (.csv)`.
    * Click `Publish` and copy the generated URL.

3.  **Update the Data Source in the Code:**
    * Open the `index.html` file in your code editor.
    * Scroll to the bottom `<script>` tag.
    * Find the `csvUrl` constant:
        ```javascript
        // --- CONFIGURATION ---
        const csvUrl = '[https://docs.google.com/spreadsheets/d/e/.../pub?gid=0&single=true&output=csv](https://docs.google.com/spreadsheets/d/e/.../pub?gid=0&single=true&output=csv)'; // <-- REPLACE THIS
        let data = [];
        ```
    * Paste your own published Google Sheet CSV link here.

4.  **Run the Dashboard:**
    * Open the `index.html` file in your browser. The dashboard will now fetch and display the data from your sheet.

## 📁 Data Structure

For the dashboard to work correctly, your Google Sheet should have columns with the following header names (case-sensitive):

* `User Name`
* `User Email`
* `Access Code Redemption Status` (Must contain "Yes" or "No")
* `# of Skill Badges Completed` (Must be a number)
* `# of Arcade Games Completed` (Must be a number)
* `All Skill Badges & Games Completed` (Must contain "Yes" or "No")
* `Google Cloud Skills Boost Profile URL`
* `Names of Completed Skill Badges` (Comma-separated list)
* `Names of Completed Arcade Games` (Comma-separated list)

## 👤 Author

Made with ❤️ by **Ezaz Ahmed Khan**
* GDG on Campus Lead, JIST
* [GitHub](https://github.com/ezeehere)
* [LinkedIn](https://www.linkedin.com/in/ezeehere)
