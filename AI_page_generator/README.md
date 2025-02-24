# AI web generator

## Version 1

Contains 5 files:
- article.html
- Article.txt
- preview.html
- Program.py
- template.html

The template.html file does not contain JavaScript code.
The template.html file does not contain content from article.html.
The preview.html file contains content from article.html.

To check how everything works in this case, simply open the preview.html file in your browser.

## Version 2

Contains 4 files:
- article.html
- Article.txt
- Program.py
- template.html

The template.html file contains JavaScript code.

For everything to work correctly:
1. Navigate to the folder containing the files
2. Open a console and enter:
   ```bash
   python -m http.server
   ```
   This will start a Python server.
   By default, the server will run at: http://localhost:8000.
3. Open your browser and go to: http://localhost:8000/template.html.

After performing these actions, the page should load correctly with the article content.

## Safety First

For security reasons, an .env file has been created which is ignored. The structure of the .env file is as follows:
```bash
OPENAI_API_KEY = "sk-proj-kp..."
```
Between "..." you should enter a valid key.