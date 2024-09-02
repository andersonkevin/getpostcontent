
# GetPostContent

GetPostContent is a Python script that automates the process of scraping content from a list of URLs and saving the extracted content into structured `.docx` files. The content is organized based on HTML tags like `<h1>`, `<h2>`, `<p>`, etc., and includes the source URL at the top of each document.

## Features

- **Automatic URL Processing**: The script processes multiple URLs provided in a list.
- **Content Structuring**: Extracted content is structured into headings, paragraphs, and lists.
- **Error Handling**: The script includes retry logic for handling network errors and incomplete responses.
- **File Naming**: Each `.docx` file is named based on the `<h1>` heading of the corresponding URL.

## Requirements

Ensure you have the following installed:

- Python 3.7+
- Required Python packages:
  - `requests`
  - `beautifulsoup4`
  - `python-docx`

You can install the necessary packages using pip:

```bash
pip install requests beautifulsoup4 python-docx
```

## Setup

1. **Clone the Repository**: Clone this repository to your local machine.

```bash
git clone https://github.com/andersonkevin/getpostcontent.git
```

2. **Navigate to the Project Directory**:

```bash
cd getpostcontent
```

3. **Create a Virtual Environment** (optional but recommended):

```bash
python3 -m venv env
source env/bin/activate  # On Windows, use `env\Scripts\activate`
```

4. **Install Dependencies**:

```bash
pip install -r requirements.txt
```

## Usage

1. **Add URLs**: Open the script file (`getpostcontent.py`) and add the URLs you want to scrape to the `urls` list.

```python
urls = [
    'https://www.example.com/article-1',
    'https://www.example.com/article-2',
    # Add more URLs here
]
```

2. **Run the Script**:

```bash
python getpostcontent.py
```

The script will process each URL, extract the content, and save it as a `.docx` file named after the article's `<h1>` title. The source URL will be included at the top of each document.

## Error Handling

- The script includes retry logic to handle network issues, such as incomplete responses or connection errors.
- If a URL cannot be processed after multiple attempts, the script will skip it and continue with the next URL.

## Contributing

Contributions are welcome! If you'd like to improve the script or add new features, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact

For any questions or issues, please open an issue on GitHub or contact the repository owner.
