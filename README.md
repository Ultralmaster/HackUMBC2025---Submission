# HackUMBC2025---Submission
Submission into categories: Best AI/ML, Best .Tech Domain, Best Use of Gemini API. The Python script uses the thumbnails of videos to download aggregate music lists.

# OCR → Gemini → YouTube Audio Downloader

This Python script performs the following:

1. Downloads a YouTube video thumbnail.
2. Runs OCR (Optical Character Recognition) on the thumbnail to extract text.
3. Filters the OCR text using Google Gemini AI.
4. Matches songs on YouTube using Gemini.
5. Downloads audio for the matched songs.
6. Keeps track of processed and failed songs.

**Basic Usage (Bash):** python SongRipper.py https://www.youtube.com/watch?v=abc123XYZ


#CLI Arguments\
##Positional Argument\
  ````url````\
Description: YouTube URL to download the thumbnail and perform OCR.\
Example: https://www.youtube.com/watch?v=abc123XYZ\


##Optional Arguments\
  ````--api_key````<br />
**Description:** Gemini AI API key. If not provided, the script will attempt to read it from GeminiAPIKey.txt.<br />
**Example:** ````--api_key YOUR_API_KEY````<br />

  ````--candidates````<br />
**Description:** Maximum number of YouTube search results to consider per song. Default: 10.<br />
**Example:** ````--candidates 20````<br />

  ````--cookies````<br />
**Description:** Path to YouTube cookies file for authenticated downloads. Default: cookies.txt.<br />
**Example:** ````--cookies mycookies.txt````<br />

  ````--tesseract````<br />
**Description:** Path to the Tesseract OCR executable. Default: C:\Program Files\Tesseract-OCR\tesseract.exe.<br />
**Example:** ````--tesseract "C:\Program Files\Tesseract-OCR\tesseract.exe"````<br />

  ````--log````<br />
**Description:** File path to save URLs that have already been downloaded. Default: downloaded.txt.<br />
**Example:** ````--log downloaded_videos.txt````<br />

  ````--cantfind````<br />
**Description:** File path to save songs that could not be found or matched. Default: cantfind.txt.<br />
**Example:** ````--cantfind missing_songs.txt````<br />

  ````--prefile````<br />
**Description:** File path for OCR prefiltered output. Default: prefiltered_ocr.txt.<br />
**Example:** ````--prefile ocr_prefilter.txt````<br />

  ````--ofile````<br />
**Description:** File path for filtered OCR output (after Gemini). Default: filtered_ocr.txt.<br />
**Example:** ````--ofile ocr_filtered.txt````<br />

  ````--outdir````<br />
**Description:** Directory where audio files will be downloaded. Default: downloads.<br />
**Example:** ````--outdir my_music_downloads````<br />

