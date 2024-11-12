Here's an updated version of your README with some emojis added for a more engaging touch:

---

# Meme Radar Program 🚨

This program scans all the sub-domains of **KnowYourMeme**, giving you an overview of all the memes created since the history of mankind. 🌐😂  
This Python program is designed to scrape subdomains from a website, filter and save them into a file, and display the results in a graphical interface using Tkinter. It allows users to find and track subdomains related to memes hosted on the "Know Your Meme" website.

## Features: ✨
- **Web Scraping**: It fetches pages containing meme subdomains. 🌍
- **Filtering**: Excludes certain irrelevant pages based on predefined filters. 🛑
- **State Management**: Keeps track of the last page processed and continues from there. 🔄
- **Subdomain Saving**: Saves found subdomains in a `.txt` file. 💾
- **GUI**: Displays the subdomains in a Tkinter window with auto-scrolling. 💻
- **Dark Mode**: The GUI interface uses a dark theme for better visibility. 🌑

---

## Requirements: 📦

- **Python 3.x**: The program requires Python 3 or later.
- **Libraries**: 
  - `requests`
  - `beautifulsoup4`
  - `tkinter`

You can install the necessary libraries using pip:
```bash
pip install requests beautifulsoup4
```

---

## Configuration: ⚙️

### File Paths:
Make sure to adjust the paths to the text files to match your system. By default, the program saves the following files to the Desktop:

1. **Subdomain File** (`sub_domains.txt`): This file contains the found subdomains.
2. **State File** (`program_state.txt`): This file tracks the last processed page number.
3. **Not Found File** (`not_found.txt`): This file logs pages with no subdomains.

### Modifying Paths:
You will need to change the file paths in the script to match your computer's directories.

For example:
```python
output_file = r"C:\Users\YourUsername\Desktop\sub_domains.txt"
state_file = r"C:\Users\YourUsername\Desktop\program_state.txt"
not_found_file = r"C:\Users\YourUsername\Desktop\not_found.txt"
```

Replace `YourUsername` with your actual username and ensure the directories exist on your computer.

---

## How to Run: 🚀

1. **Modify Paths**: Open the script and ensure that the paths for the `.txt` files match your system configuration.
   
2. **Start the Program**: Run the Python script using a terminal or command prompt:
   ```bash
   python subdomain_finder.py
   ```

3. **View Results**: As the program runs, the subdomains will be displayed in a Tkinter window, and the results will be saved in the `sub_domains.txt` file.

4. **Stop the Program**: You can stop the program at any time by clicking the **Stop** button in the Tkinter window. 🛑

---

## Program Behavior: 🧠

1. **Pagination**: The program scrapes subdomains across multiple pages. It starts at the first page and continues to the next page until all subdomains are found.
2. **Subdomain Extraction**: Subdomains are extracted from links containing `/memes/` and are filtered to exclude unwanted pages like "researching", "guidelines", etc. 🔍
3. **State Saving**: The program saves the current page number so that if you stop the program, it will continue from where it left off when restarted. 📝
4. **Subdomain Saving**: Each unique subdomain is saved into `sub_domains.txt`, with duplicate subdomains being ignored. 🚫

---

## Additional Notes: 📌

- **Error Handling**: If there is an issue with the web request (e.g., connection error or invalid response), the program will stop scraping. ⚠️
- **No Subdomains Found**: If no subdomains are found on a page, the page number is saved in `not_found.txt` for reference. 📝
- **ASCII Art**: If the output file is empty, the program will append an ASCII art header to `sub_domains.txt`. 🎨

---

## Example Output: 🖥️

The `sub_domains.txt` file will look like this after the program has run:
```
___  ___                     ______          _            
|  \/  |                     | ___ \        | |           
| .  . | ___ _ __ ___   ___  | |_/ /__ _  __| | __ _ _ __ 
| |\/| |/ _ \ '_ ` _ \ / _ \ |    // _` |/ _` |/ _` | '__| 
| |  | |  __/ | | | | |  __/ | |\ \ (_| | (_| | (_| | |   
\_|  |_/\___|_| |_| |_|\___| \_| \_\__,_|\__,_|\__,_|_|   
                                                          
                                                          
meme-subdomain-1
meme-subdomain-2
...
```

In the Tkinter interface, you will see a list of subdomains as they are found. 💡

---

## Troubleshooting: 🔧

- **No Data Found**: Ensure that the URL base is correct and the website is accessible. Also, check the filtering logic to ensure it's not excluding too many pages. 🌐
- **File Permission Errors**: Ensure that the program has write access to the specified file paths. 🔑
- **Missing Libraries**: If you get an error about missing libraries, ensure they are installed using `pip`. 📥

---

## License: 📝

This program is open-source and free to use. You can modify and distribute it as you wish, but please ensure you respect the terms of any data you're scraping. Always comply with the website's terms of service. 📜

--- 

Enjoy finding meme subdomains! 😄
