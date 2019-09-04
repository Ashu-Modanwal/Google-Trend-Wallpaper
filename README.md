# Google-Trend-Wallpaper
A python and shell script to set the wallpaper to a wordcloud of the most trending google searches. 

This project is inspired from [process-wallpaper](https://github.com/anirudhajith/process-wallpaper). You can check it out for the wordcloud of most resource hungry processes running in your system.

![Screenshot](https://github.com/shardul08/Google-Trend-Wallpaper/blob/master/screenshot.png)  


## Dependencies
* `python3`
* `gsettings` or `feh`  To set the generated wordcloud as the wallpaper
* `xvfb`  To simulate a display and run everything in memory
### Python dependencies
* `selenium`  To scrape the data from [Google trends](https://trends.google.com/trends/trendingsearches/daily?geo=IN)
* `pyvirtualdisplay` Python wrapper for `xvfb`
* `wordcloud` To generate the wordcloud
* `PIL`  Python imaging library

**NOTE** You will need to download the webdriver for `selenium`. [Geckodriver](https://github.com/mozilla/geckodriver/) (webdriver for firefox) can be downloaded from [here](https://github.com/mozilla/geckodriver/releases). 

## Setup
* Clone this repo
```
git clone https://github.com/shardul08/Google-Trend-Wallpaper.git
```
* Change directory to the repo
```
cd Google-Trend-Wallpaper
```
* Run `setup.sh` with
```
./setup.sh
```
This will install all the required dependencies and set the wallpaper.

## Usage
Run `./updateWallpaper.sh` to update the wallpaper to the wordcloud of the latest trends.

You can set your region/country to get the trending searches in `line #12` of [`generateWallpaper.py`](https://github.com/shardul08/Google-Trend-Wallpaper/blob/master/generateWallpaper.py)

You can set the number of days for which you want the trending searches in `line #13` of [`generateWallpaper.py`](https://github.com/shardul08/Google-Trend-Wallpaper/blob/master/generateWallpaper.py)

**NOTE** If the wallpaper is not set automatically, you can set `wallpaper.png` as the wallpaper manually.
