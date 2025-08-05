# 🔁 Codewars Kata Sync to GitHub V1.0

A simple and fully automated Python tool that **fetches completed Codewars katas (exercises + solutions)** for a given user and **pushes them to a personal GitHub repository**.

---

## 🚀 Features

- 🔍 Fetches all completed katas from a user's Codewars profile.
- 📥 Retrieves the user's submitted solution for each kata via web scraping.
- 📂 Organizes files locally for version control.
- ☁️ Automatically pushes solutions to a GitHub repository using Git.

---

## ⚙️ Requirements

- Python 3.8+
- A Codewars account
- A GitHub repository (empty)
- Git installed on your system
- Google Chrome (used by Selenium for login)
- GitHub access token (using HTTPS)

---

## 📦 Installation

1. Clone this project or download the source code.
2. Navigate into the project folder:
   ```bash
   cd automate_codewars_to_github
3. Install dependencies:
    ```bash
    pip install -r requirements.txt

## ⚙️ Configuration

1. Create a .env file in the project root directory.
2. Add the following environment variables to it:
    ```bash
    USERNAME=your_codewars_username
    EMAIL=your_codewars_email
    PWD=your_codewars_password
    GITHUB_DEPOT_URL=https://github.com/yourusername/your-repo.git

🔐 Never commit your .env file to GitHub. It contains sensitive information.

## 📁 .gitignore Example

Create a .gitignore file in the project root with the following content:
    ```bash
    .env
    bd.json
    bd.py
    file_gestion.py
    main.py
    codewars.py
    github.py

This ensures your config and internal scripts are not pushed to your GitHub repo.

## ▶️ Usage

python main.py

The tool will:

1. Log in to Codewars via Selenium.

2. Fetch all completed kata titles and solutions.

3. Save them locally in an organized folder.

4. Commit and push all solutions to your specified GitHub repo.

## 📌 Notes

Codewars authentication is handled using Selenium, simulating real browser login.

Environment variables are loaded with python-dotenv.

Git operations (add, commit, push) are handled via Python and subprocess.

Your Codewars solutions are organized and version-controlled in GitHub.

## 🔒 Security Tips

Always add .env to your .gitignore to avoid leaking sensitive credentials.

Consider using GitHub SSH or Personal Access Tokens instead of password-based HTTPS for better security.

Change your .env values frequently if you store real credentials.


## 💡 Ideas for Improvements


Allow optional GitHub repo creation via the GitHub API.

Support for multiple users or batch export.

Convert solutions to Markdown format for better readability.

GitHub Action integration for scheduled syncing.

## 🧑‍💻 Author
Developed with ❤️ by Yepie Daniel
Feel free to fork, improve, or contribute.

## 📄 License
This project is open source and free to use for educational or personal purposes.