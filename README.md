# 🔍 Automated Domain Reconnaissance Workflow

A light, fast, and automated **GitHub Actions Workflow** designed for passive subdomain enumeration and URL discovery (including JavaScript endpoints) for authorized security testing and bug bounty engagements.

---

## 🚀 Features

* **Passive Subdomain Enumeration:** Utilizes `subfinder` to collect subdomains without directly probing targets.
* **URL & Endpoint Discovery:** Aggregates historical URL data using `gau` (GetAllUrls) and `waybackurls`.
* **JavaScript File Filtering:** Automatically extracts and isolates `.js` file endpoints for focused analysis.
* **Parallel Execution:** Uses concurrent threads to speed up data collection.
* **Artifact Export:** Saves clean, deduplicated outputs (`subdomains.txt`, `all_urls.txt`, `js_urls.txt`) directly to GitHub Action artifacts.

---

## 🛠️ Tools Used

* [Subfinder](https://github.com/projectdiscovery/subfinder) - Subdomain discovery tool.
* [GAU](https://github.com/lc/gau) - Fetch known URLs from AlienVault's OTX, Wayback Machine, and Common Crawl.
* [Waybackurls](https://github.com/tomnomnom/waybackurls) - Fetch URLs from the Wayback Machine.

---

## 📋 How to Use

1. **Fork or Add to Your Repository:**
   Place the workflow YAML file inside `.github/workflows/recon.yml`.

2. **Run the Workflow:**
   * Go to the **Actions** tab in your GitHub repository.
   * Select **Recon Automation** from the workflow list.
   * Click **Run workflow**.
   * Enter the **Target domain** (e.g., `example.com`).

3. **Download Results:**
   * Once the workflow finishes, scroll down to the **Artifacts** section at the bottom of the run page.
   * Download `recon-results-<domain>.zip`.

---

## 📁 Output Files

| File | Description |
| :--- | :--- |
| `subdomains.txt` | Cleaned and deduplicated list of active subdomains found. |
| `all_urls.txt` | Complete list of unique historical URLs gathered. |
| `js_urls.txt` | Isolated list of JavaScript URLs extracted for review. |

---

## ⚠️ Disclaimer

> **Educational and Authorized Use Only**  
> This workflow is built strictly for **authorized penetration testing, bug bounty programs, and security research** on assets you own or have explicit written permission to test. Unauthorized scanning of targets is illegal.
