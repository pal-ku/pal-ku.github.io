# PAL-KU Lab Website

Welcome to the PAL-KU lab website repository. This site is built using **Hugo** and is designed to be easily updated by lab members.

## How to Contribute

Detailed instructions for adding content are located directly within the relevant data and content files.

### 1. Adding Publications (The Database)
-   **File**: [`data/publications.yml`](data/publications.yml)
-   **Purpose**: This is the "Master Record" of every citation. It's stored as data so we can automatically generate BibTeX, count entries, and sort them in a clean list without creating hundreds of files.
-   **Instructions**: Refer to the commented section at the **top of the file**.

### 2. Adding News Articles (The Feed)
-   **Directory**: [`content/news/`](content/news/)
-   **Purpose**: Standalone stories or announcements with their own pages and URLs.
-   **Instructions**: Create a new `.md` file in this directory. Reference existing files for the front matter format.

### 3. Featured Article Posts (The Showcases)
-   **Directory**: [`content/featured/`](content/featured/)
-   **Purpose**: If you want to do a "Deep Dive" or "Featured Spotlight" on a specific paper with detailed text and images, create a page here. 
-   **Linking**: Use the `related_publication_ids` in the front matter to link it back to the citation in the data file. If you do this, the news item will be displayed on the publications page with a "Read Story" button.

### 4. Updating the Project Checklist
-   **File**: [`TODO.md`](TODO.md)
-   **Instructions**: Tracks overall website progress. Mark tasks as complete when done.

---
For technical issues or structural changes, please consult the lab lead or the repository administrator.
