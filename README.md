# Arc Pinned Tabs to HTML Bookmarks Converter

## Overview

This project provides a script for converting pinned tabs in the **Arc Browser** to standard HTML bookmarks file. These bookmarks can then be imported into any web browser.

This addresses the lack of a pinned tabs export feature in Arc Browser.

## Requirements

- Python 3.9 or higher
- Arc Browser installed

## Installation

1. Clone the repository: `git clone git@github.com:ivnvxd/arc-export.git`
2. Navigate to the project folder: `cd arc-export`

or download using `curl`:

```sh
curl -o main.py https://raw.githubusercontent.com/ivnvxd/arc-export/main/main.py
```

## Usage

Run the `main.py` script from the command line:

```sh
python3 main.py [-h] [-s] [-o OUTPUT] [-v] [--version]

# or if there is an error:
python main.py [-h] [-s] [-o OUTPUT] [-v] [--version]
```

### Troubleshooting

If you encounter any problems, manually copy the `StorableSidebar.json` file from the `~/Library/Application Support/Arc/` directory to the project's directory and run the script again.

## Features

The script supports various command-line options for enhanced functionality:

- **Show help message and exit**

  - `-h`, `--help`

- **Silence output**

  - `-s`, `--silent`

- **Specify the output file path**

  - `-o OUTPUT`, `--output OUTPUT`

- **Enable verbose output**

  - `-v`, `--verbose`

- **Print the git short hash and commit time**
  - `--version`

Example usage:

`python3 main.py -v -o my_bookmarks.html`

![Example Usage](example.gif)

## How It Works

1. **Read JSON**: Reads the `StorableSidebar.json` file from the Arc Browser's directory _or_ the project's directory.
2. **Convert Data**: Converts the JSON data into a hierarchical bookmarks dictionary.
3. **Generate HTML**: Transforms the bookmarks dictionary into an HTML file.
4. **Write HTML**: Saves the HTML file with a timestamp, allowing it to be imported into any web browser.

## Contributions

Contributions are very welcome. Please submit a pull request or create an issue.

## Support

Thank you for using this project! If you find it helpful and would like to support my work, kindly consider buying me a coffee. Your support is greatly appreciated!

<a href="https://www.buymeacoffee.com/ivnvxd" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

And do not forget to give the project a star if you like it! :star:

## License

This project is licensed under the MIT License.
