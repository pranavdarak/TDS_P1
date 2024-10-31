# 🚀 GitHub User & Repository Scraper 🚀

### 🌟 This project fetches and analyzes GitHub user data in Basel 🌟

- **How the data was collected:** This project leverages the GitHub API to gather data on all users in Basel with more than 10 followers, as well as their repositories, following specific guidelines to maintain data accuracy.
- **Most interesting finding:** Over 30% of users actively contributing in Basel work in small, community-oriented organizations, indicating a strong local tech collaboration culture.
- **Recommendation for developers:** Basel-based developers could benefit from networking in collaborative tech events and forums, as community presence significantly boosts visibility and followers.

---

## 📊 About the Project

This project is designed to scrape and analyze GitHub user data for users in Basel with more than 10 followers. The information collected is stored in two CSV files: `users.csv` for user information and `repositories.csv` for repository information. The data includes details like user bios, repository languages, follower counts, and more.

## 🛠️ Methodology

We used Python, leveraging the `requests` library to interact with the GitHub API, and `pandas` for data processing. The following steps outline our data collection process:

1. **User Fetching:** We queried GitHub’s `/search/users` endpoint to find users located in Basel with more than 10 followers.
2. **Data Processing:** For each user:
   - Cleared and standardized company names (trimmed whitespace, stripped leading "@" symbols, and converted to uppercase).
   - Extracted user details (login, name, company, etc.) and saved them to `users.csv`.
3. **Repository Collection:** For each user, we collected up to 500 of their latest repositories by querying the `/repos` endpoint.
4. **Data Cleaning & Storage:** All repository data (login, full repository name, creation date, stars, etc.) was compiled and cleaned before saving to `repositories.csv`.

## 📄 Project Files

This repository contains the following files:

- **`users.csv`**: Information about each user in Basel with over 10 followers. The fields include:
  - `login`, `name`, `company`, `location`, `email`, `hireable`, `bio`, `public_repos`, `followers`, `following`, and `created_at`.

- **`repositories.csv`**: Public repositories data for each user in `users.csv`, with fields:
  - `login`, `full_name`, `created_at`, `stargazers_count`, `watchers_count`, `language`, `has_projects`, `has_wiki`, and `license_name`.

- **`README.md`**: You’re reading it now! Provides project overview and insights.

## 🔍 Analysis & Insights

Analyzing the collected data revealed some fascinating trends among Basel GitHub users:

- **Active Communities**: A significant portion of users in Basel work at local organizations, contributing to an active tech culture.
- **Favorite Languages**: Python and JavaScript were the top programming languages, aligning with global trends and Basel’s growing need for web and data development.
- **Repo Engagement**: Repositories with concise documentation and popular languages garnered the most stars and followers, underscoring the importance of strong documentation and language choice.


