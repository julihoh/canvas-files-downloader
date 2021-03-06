# canvas-files-downloader

Downloads your Canvas course files, group submissions, and user submissions

## Usage

* Requires Python 3
* Create `.env`
  * Generate an access token for testing
    * https://canvas.instructure.com/doc/api/file.oauth.html#manual-token-generation
    * ```
      ACCESS_TOKEN=
      ```
    
    * Put your access token after the equals sign
  
  * Setup canvas installation url:
  ```
      CANVAS_URL=your canvas url (eg. canvas.vu.nl)
   ```
  * (optional) targer folder (./files by default):
  ```
      FOLDER=~/canvas_files
   ```
* Create a virtual environment and activate it
  * `python3 -m venv venv`
  * `source venv/bin/activate`
* Install dependencies
  * `pip install -r requirements.txt`
* Run the script
  * `python canvas-files-downloader.py`
* Files will be downloaded to `files/` or the folder specified in the configuration
* Usage with multiple canvas accounts/installations: simply call the script for each installation url and/or authentication token from a script:
```
ACCESS_TOKEN=... CANVAS_URL=first_url python canvas-files-download.py
ACCESS_TOKEN=... CANVAS_URL=second_url python canvas-files-download.py
```

