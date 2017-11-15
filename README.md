# pandoc-docs

## General

*pandoc-docs* is a small bash script which searches for all .md - files and converts them with pandoc to beautiful LaTeX-PDFs.

The script watches a directory and checks each 10 seconds if there are changes to .md-files and if so, starts pandoc to update the pdf.

## Requirements

- A installed LaTeX - distribution like [TeX Live](https://www.tug.org/texlive/)
- [pandoc](https://pandoc.org/installing.html)

## Installation

1. Clone this repo: `git clone https://github.com/FHefner/pandoc-docs`
2. Copy the script to a directory which is in your `$PATH`, under most linux distros e.g. `sudo cp pandoc-docs /usr/bin`
3. Set the executable flag for the binary: `sudo chmod +x /usr/bin/pandoc-docs`

## Usage

1. Change to the directory containing your .md - files
2. Start the script in a terminal and keep it running (it's a endless-loop, you can kill the process with *ctrl-c*): `pandoc-docs`
	1. You can use the optional paramter **-n** for adding numbered sections: `pandoc-docs -n`
3. Keep editing your .md - files with your favorite editor. Each time you save the file, the .pdf gets generated again.