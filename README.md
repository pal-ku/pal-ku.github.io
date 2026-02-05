# PAL-KU Lab Website

Welcome to the PAL-KU lab website repository. This site is built using **Hugo** and is designed to be easily updated by lab members.

## How to Contribute

Detailed instructions for adding content are located directly within the relevant data and content files.

### 1. Local Testing
- **Install Hugo**: Ensure you have the [Hugo Extended version](https://gohugo.io/installation/) installed.
- **Run Server**: Execute `hugo server -D` in the root directory.
- **Check Manually**: Open `http://localhost:1313` and verify your changes. Look for any errors or layout issues.

> [!IMPORTANT]
> **The Golden Rule of `public/`**: Never commit the `public/` folder. We let GitHub Actions handle the build in the cloud. Your local folder stays clean, and "compiled" files never touch the repository.

### 2. Automated Build Checks
This repository uses GitHub Actions to automatically validate changes:
- **Status Checks**: Every pull request and push to `main` triggers a build test.
- **Validation**: Check the "Actions" tab or the merge box in your PR to ensure the build passes.
- **Deployment**: Only successful builds on the `main` branch are deployed to the live site.

### 3. Safe-Proofing your Workspace
- **Check `.gitignore`**: Ensure it contains a line for `public/` to prevent accidental commits of generated files.
- **Clean up**: If you accidentally run `hugo` without the `server` flag, you can safely delete the `public/` folder.

### 4. Adding Publications (The Database)
-   **File**: [`data/publications.yml`](data/publications.yml)
-   **Purpose**: This is the "Master Record" of every citation. It's stored as data so we can automatically generate BibTeX, count entries, and sort them in a clean list without creating hundreds of files.
-   **Instructions**: Refer to the commented section at the **top of the file**.

### 5. Adding News Articles (The Feed)
-   **Directory**: [`content/news/`](content/news/)
-   **Purpose**: Standalone stories or announcements with their own pages and URLs.
-   **Instructions**: Create a new `.md` file in this directory. Reference existing files for the front matter format.

### 6. Featured Article Posts (The Showcases)
-   **Directory**: [`content/featured/`](content/featured/)
-   **Purpose**: If you want to do a "Deep Dive" or "Featured Spotlight" on a specific paper with detailed text and images, create a page here. 
-   **Linking**: Use the `related_publication_ids` in the front matter to link it back to the citation in the data file. If you do this, the news item will be displayed on the publications page with a "Read Story" button.

### 4. Updating the Project Checklist
-   **File**: [`TODO.md`](TODO.md)
-   **Instructions**: Tracks overall website progress. Mark tasks as complete when done.

---
For technical issues or structural changes, please consult the lab lead or the repository administrator.
