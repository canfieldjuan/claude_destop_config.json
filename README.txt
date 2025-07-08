**README.txt – Claude Desktop Config + MCP Tools Guide**

---

### 🔧 Overview:

This file (`claude_desktop_config.json`) is used to configure the Claude Desktop app. It sets the UI preferences and defines a list of active **MCP servers** (Model Context Protocol microservices) that power Claude’s capabilities across memory, databases, browsers, files, and automation.

---

### ⚙️ General Settings:

* **darkMode**: `"light"` or `"dark"` – Controls UI theme.
* **scale**: UI scale factor (0 = default).
* **locale**: Language/region code (e.g., `en-US`).

---

### 💻 Window Placement:

* **quickWindowPosition**: Defines where Claude launches on screen.

  * Uses absolute screen position and detects monitor specs.
  * Monitor label: `PHL 271V8LB`
  * Screen size: 1920×1080
  * Display frequency: 60Hz

---

### 🔌 Total MCP Tools Enabled: **12**

Each tool adds specific functionality to Claude’s local environment:

| #  | Tool Name               | What It Does                                                                           |
| -- | ----------------------- | -------------------------------------------------------------------------------------- |
| 1  | **memory**              | Stores and recalls session memory. Good for short-term local state.                    |
| 2  | **github**              | Accesses GitHub repos to read/write code, manage issues, and track versioning.         |
| 3  | **sequential-thinking** | Enables step-by-step reasoning and complex task handling logic.                        |
| 4  | **puppeteer**           | Headless browser automation (e.g., scraping, screenshots, navigating sites).           |
| 5  | **sqlite**              | Connects to a local SQLite database at: `local_data.db`                                |
| 6  | **browsermcp**          | Another browser-based automation tool for focused context access.                      |
| 7  | **pdf-generator**       | Converts content to PDF using a GitHub microservice.                                   |
| 8  | **excel**               | Parses Excel spreadsheets. Handles large sheets up to 4000 cells per page.             |
| 9  | **playwright**          | Browser automation like Puppeteer, but supports more browsers (e.g., WebKit, Firefox). |
| 10 | **file-converter**      | Converts files using Puppeteer (e.g., HTML→PDF, DOCX→PDF).                             |
| 11 | **mysql**               | Full access to a MySQL DB with all operations enabled (insert/update/delete).          |
| 12 | **desktop-commander**   | Executes local desktop commands, automating file/script actions.                       |

---

### 🧩 Categorized Summary:

**Storage & Data:**
* `memory`, `sqlite`, `mysql`, `excel`

**Web Automation:**
* `puppeteer`, `browsermcp`, `playwright`, `file-converter`

**Logic & Execution:**
* `sequential-thinking`, `desktop-commander`

**External Services:**
* `github`, `pdf-generator`

---

### 🔐 Notes & Warnings:

* `GITHUB_PERSONAL_ACCESS_TOKEN` is required for GitHub access – set this securely via env vars.
* MySQL server is **fully open** for modifications — **do not expose to public internet**.
* Make sure Node.js and `npx` are installed globally.
* Avoid sharing this config as-is due to potential sensitive tokens and local paths.

---

Let me know if you want a Markdown version (`README.md`) or auto-generate this from code in future projects.
