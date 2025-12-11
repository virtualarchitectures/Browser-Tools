# Browser Tools

A collection of browser-based HTML+JavaScript tools for various tasks. Each tool has been built with the aid of LLMs and agentic coding tools. In each case AI has been used to tailor the tool to my own practical needs, and in broad alignment with the kinds of principles outlined under the headings of [malleable software](https://www.inkandswitch.com/essay/malleable-software/) and [resonant computing](https://resonantcomputing.org/). All tools run entirely in your browser with no server-side processing.

## Features

- 🚀 No server-side processing required
- 🔒 All data stays in your browser
- 📱 Works on any modern browser
- 🔍 Search functionality to find tools quickly

## Usage

Navigate to [https://virtualarchitectures.github.io/Browser-Tools/](https://virtualarchitectures.github.io/Browser-Tools/) in your browser to access the tools.

## Available Tools

### Data Processing

- **[CSV to JSON Converter](csv-to-json.html)** — convert CSV files to JSON format with support for dot notation parsing, multiple output formats (JSON Array, JSON Lines), and table preview
- **[JSON to CSV Converter](json-to-csv.html)** — convert JSON files to CSV format with support for nested objects, array handling, and table preview

### Digital Forensics

- **[Email Header Analysis](email-header-analysis.html)** — analyse and highlight email headers with syntax highlighting for IPs, emails, and URLs

### Documents and Text

- **[OCR Reader](ocr-reader.html)** — extract text from images and PDF files using optical character recognition with side-by-side preview
- **[PDF Metadata Viewer](pdf-metadata.html)** — extract and view PDF metadata including title, author, dates, permissions, and security settings
- **[PDF to Images](pdf-to-images.html)** — extract high-quality images of pages from PDF documents with adjustable DPI and format options (PNG, JPEG, WebP)
- **[Text Chunking Tool](text-chunking.html)** — split text documents into manageable chunks using multiple strategies (character count, word count, sentence-based, paragraph-based, recursive split, sliding window) with configurable overlap and export to CSV
- **[Text Diff](text-diff.html)** — compare two text blocks and highlight added and removed content
- **[Text Tools](text-tools.html)** — text manipulation toolkit with case transformation, sorting, whitespace cleaning, encoding/decoding (Base64, URL), find & replace, and text tokenization

### OSINT

- **[Identifier Extractor](identifier-extractor.html)** — extract and analyse URLs, email addresses, IPv4/IPv6 addresses, phone numbers, and MAC addresses from text with filtering, sorting, and export options

### Image

- **[EXIF Data Viewer](exif-viewer.html)** — extract and view EXIF metadata from photos including camera settings, GPS location, and timestamps
- **[Image Resize Tool](image-resize.html)** — resize images by percentage or pixels with precise scale factor control for copying scale factor to other images
- **[Pixel Coordinates](pixel-coords.html)** — click on images to capture and record pixel coordinates

### Media

- **[Multi-Webcam Viewer](webcam-viewer.html)** — view multiple webcam feeds simultaneously with support for YouTube embeds, direct video streams (MP4, M3U8, HLS), and iframe-compatible sources
- **[Scene Detection Tool](scene-detection.html)** — automatically detect scene changes in videos using frame analysis with adjustable sensitivity, minimum scene duration, and sample rate controls
- **[Transcription Tool](transcribe.html)** — transcribe audio and video files with keyboard shortcuts, timestamps, and speed control

### Maps and Spatial Data

- **[Feature Service Viewer](feature-service-viewer.html)** — load and visualize ArcGIS Feature Services and MapServer layers on an interactive map
- **[GeoJSON Viewer](geojson-viewer.html)** — visualize and explore GeoJSON files on an interactive map

### Natural Language Processing (NLP)

- **[Named Entity Recognition](named-entity-recognition.html)** — extract and identify named entities from text including people, places and organisations using natural language processing
- **[Word Frequency Counter](word-frequency.html)** — analyze word frequency, discover common phrases with n-grams (bigrams, trigrams, 4-grams, 5-grams), and get detailed text statistics with customisable stop word filtering

### Programming and Development

- **[GitHub Commits Viewer](github-commits.html)** — view and export commit history from GitHub repositories with support for CSV, JSON, and Markdown exports

### Web Development

- **[Favicon Generator](favicon-generator.html)** — generate favicons in multiple sizes and formats including SVG, ICO, Apple Touch Icons, and Android icons

### Web Privacy & Security

- **[Browser Fingerprint Viewer](browser-fingerprint.html)** — view browser fingerprint data that websites can collect including canvas fingerprinting, WebGL info, audio context, detected fonts, and device characteristics
- **[Cookie & Storage Analysis](cookie-storage-analysis.html)** — examine all data websites can store on your device including cookies, localStorage, sessionStorage, IndexedDB, cache storage, and service workers with detailed analysis

## Acknowledgement

This set of tools has been developed using a range of agentic coding tools. This collection was inspired by [Simon Willison's](https://simonwillison.net/) experiment in prompt-driven development, using LLMs to develop his own set of standalone HTML + Javascript tools. Simon's code lives on GitHub in [simonw/tools](https://github.com/simonw/tools) and many of his tools used the Claude custom instructions [described here](https://simonwillison.net/2024/Dec/19/one-shot-python-tools/#custom-instructions).
