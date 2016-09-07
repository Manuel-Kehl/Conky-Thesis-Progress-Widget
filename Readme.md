# Conky Thesis Progress Widget

This conky configuration displays a simple overview about your thesis progress (word count) as well as the remaining number of days until the deadline.
I wrote it for my own MSc thesis and it helped to make the whole thing a lot more fun :wink:

![A screenshot of the conky setup](screenshot.png)

## Dependencies

These instructions are for Ubuntu. Package names on other distributions may vary.

1. conky (>= 1.10): `sudo apt-get install conky`
2. exiftool: `sudo apt-get install libimage-exiftool-perl`
3. pdftotext: `sudo apt-get install poppler-utils`
4. FontAwesome: `sudo apt-get install fonts-font-awesome`
5. Purisa Font: `sudo apt-get install fonts-tlwg-purisa`

## Installation

1. Copy the conky configuration to your home directory: `cp conkyrc ~/.conkyrc`
2. Make sure everything in `scripts` is executable and in your `PATH`

## Setup

You will want to adapt 2 files:
 - Change the path to the PDF file in `.conkyrc`
 - Change the deadline date UNIX timestamp in `.conkyrc`
 - Change the amount of start/end pages to skip in `.conkyrc` (parameters 1 and 2 to `pdfWordCount`)
 - Change the *word exclusion rules* by adding/removing/adapting `sed` calls in `pdfWordCount`

