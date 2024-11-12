# Meme Information Extraction

This script extracts meme information from the **Know Your Meme** website using subdomains listed in a given file. The extracted information is saved to a text file, while links without relevant information are recorded in a separate file for later review.

## Prerequisites

- Python 3.x
- The following libraries:
  - `requests`
  - `beautifulsoup4`
  - `re`
  - `json`
  
You can install the required dependencies via `pip`:
```bash
pip install requests beautifulsoup4
```

## Description

### How It Works

1. The script reads a text file containing subdomains (one subdomain per line) located at:
   - `C:/Users/natsu/Desktop/sous_domaines.txt`
   
2. For each subdomain, it constructs a full URL to the corresponding page on **Know Your Meme**.

3. The script attempts to retrieve relevant information about each meme from the page:
   - If the page corresponds to an event (identified by `/events` in the URL), it looks for a JSON data block.
   - Otherwise, it searches the main section of the page to extract text from paragraphs while filtering out references in square brackets.

4. The extracted information is cleaned:
   - ASCII art and sentences containing the word "warning" are removed.
   - References in square brackets are filtered out.

5. The cleaned information is saved in a file called `meme_info.txt`.

6. Links that do not contain relevant information are saved in `texte_notfound.txt`.

### Output File Structure

- `meme_info.txt`: This file contains the extracted information for each meme, in a specific format.
- `texte_notfound.txt`: This file contains the links where no relevant information was found.

### Example Output

#### meme_info.txt
```
292. **Example Meme**: Description of the meme here...
...
```

#### texte_notfound.txt
```
293. **Meme Not Found**: Unavailable.
...
```

### Parameters

- The script assumes the `sous_domaines.txt` file is located on the user's desktop at the specified path.
- You can adjust this path by modifying the `sous_domaines_path` variable.

## Usage

1. Place the `sous_domaines.txt` file containing the subdomains in the specified directory.
2. Run the Python script to start extracting information.
3. Check the output files (`meme_info.txt` and `texte_notfound.txt`) for the results.

## Troubleshooting

- **Error: File 'sous_domaines.txt' not found**: Ensure the file exists at the specified location.
- **HTTP Error 410**: Some pages have been removed or are inaccessible, and these pages will be ignored.

## License

This project is licensed under the [MIT License](LICENSE).
```

This provides a full overview of your script and clear instructions for usage.