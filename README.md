```markdown
# Meme Subdomain Scraper 🕵️‍♂️🌐

This Python program scrapes and collects subdomains from **Know Your Meme**. It processes multiple pages of meme categories, filters unwanted content, and saves the results in a text file. The program uses Tkinter to display the found subdomains in a graphical interface.

## Features ✨
- **Web Scraping**: Fetches subdomains from the Know Your Meme website. 🌍
- **Filtering**: Excludes irrelevant pages like "researching" and "guidelines". 🚫
- **State Management**: Tracks and continues from the last processed page. 🔄
- **Subdomain Saving**: Saves found subdomains to a `.txt` file. 💾
- **GUI Interface**: Displays subdomains with auto-scrolling in a Tkinter window. 💻
- **Dark Mode**: The GUI has a dark theme for a sleek and comfortable experience. 🌑

---

## Requirements 📦

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

## Configuration ⚙️

### File Paths:
Make sure to adjust the paths to the text files to match your system. By default, the program saves the following files to the Desktop:

1. **Subdomain File** (`sous_domaines.txt`): Contains the list of found subdomains.
2. **State File** (`etat_programme.txt`): Tracks the last processed page number.
3. **Not Found File** (`pas_trouves.txt`): Logs pages with no subdomains.

### Modifying Paths:
Update the file paths in the script to match your computer's directories. For example:

```python
output_file = r"C:\Users\YourUsername\Desktop\sous_domaines.txt"
state_file = r"C:\Users\YourUsername\Desktop\etat_programme.txt"
not_found_file = r"C:\Users\YourUsername\Desktop\pas_trouves.txt"
```

Replace `YourUsername` with your actual username and ensure the directories exist on your computer.

---

## How to Run 🚀

1. **Modify Paths**: Open the script and make sure the file paths for the `.txt` files match your system configuration.
   
2. **Start the Program**: Run the Python script using a terminal or command prompt:
   ```bash
   python scraper.py
   ```

3. **View Results**: As the program scrapes, subdomains will be displayed in the Tkinter window, and the results will be saved to `sous_domaines.txt`.

4. **Stop the Program**: Click the **Stop** button in the Tkinter window to stop the program at any time. 🛑

---

## Program Behavior 🧠

1. **Pagination**: The program scrapes subdomains across multiple pages. It starts at page 1 and continues to the next until all pages are processed (up to 2605).
2. **Subdomain Extraction**: Subdomains are extracted from links containing `/memes/` and filtered to exclude pages like "researching", "guidelines", and others. 🔍
3. **State Saving**: The program saves the current page number so it can continue from where it left off when restarted. 📝
4. **Subdomain Saving**: Only unique subdomains are saved to `sous_domaines.txt`, and duplicates are ignored. 🚫

---

## Additional Notes 📌

- **Error Handling**: If there's an issue with a web request (e.g., connection error or invalid response), the program will stop scraping. ⚠️
- **No Subdomains Found**: Pages with no subdomains will have their page number saved in `pas_trouves.txt`. 📝
- **ASCII Art**: If the `sous_domaines.txt` file is empty, an ASCII art header will be added. 🎨

---

## Example Output 🖥️

After running the program, `sous_domaines.txt` will contain the following:

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

In the Tkinter interface, subdomains are displayed as they are found. 💡

---

## Troubleshooting 🔧

- **No Data Found**: Ensure the URL base is correct, and the website is accessible. Also, check the filtering logic to make sure it's not excluding too many pages. 🌐
- **File Permission Issues**: Ensure the program has write access to the specified file paths. 🔑
- **Missing Libraries**: If you encounter errors about missing libraries, install them using `pip`. 📥

---

## License 📝

This program is open-source and free to use. You can modify and distribute it as you wish, but please respect the terms of the data you're scraping. Always comply with the website's terms of service. 📜

---

Enjoy scraping meme subdomains! 😄
```

### Key Changes:
- The README has been adjusted to match the details of your code, with a clearer description of the functionality and setup.
- Emojis have been added for a more engaging and fun layout.
- Specific file paths and examples are highlighted for easy configuration.
