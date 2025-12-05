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

### Data

- **[CSV to JSON Converter](csv-to-json.html)** — convert CSV files to JSON format with support for dot notation parsing, multiple output formats (JSON Array, JSON Lines), and table preview
- **[JSON to CSV Converter](json-to-csv.html)** — convert JSON files to CSV format with support for nested objects, array handling, and table preview

### Digital forensics

- **[Email Header Analysis](email-header-analysis.html)** — analyse and highlight email headers with syntax highlighting for IPs, emails, and URLs

### Image

- **[EXIF Data Viewer](exif-viewer.html)** — extract and view EXIF metadata from photos including camera settings, GPS location, and timestamps
- **[Image Resize Tool](image-resize.html)** — resize images by percentage or pixels with precise scale factor control for copying scale factor to other images
- **[Pixel Coordinates](pixel-coords.html)** — click on images to capture and record pixel coordinates

### Media

- **[Multi-Webcam Viewer](webcam-viewer.html)** — view multiple webcam feeds simultaneously with support for YouTube embeds, direct video streams (MP4, M3U8, HLS), and iframe-compatible sources
- **[Transcription Tool](transcribe.html)** — transcribe audio and video files with keyboard shortcuts, timestamps, and speed control

### Maps and spatial data

- **[GeoJSON Viewer](geojson-viewer.html)** — visualize and explore GeoJSON files on an interactive map

### Text and documents

- **[Link Finder](link-finder.html)** — extract URLs and email addresses from text with filtering, sorting, and export options
- **[OCR Reader](ocr-reader.html)** — extract text from images and PDF files using optical character recognition with side-by-side preview
- **[PDF Metadata Viewer](pdf-metadata.html)** — extract and view PDF metadata including title, author, dates, permissions, and security settings
- **[Text Diff Tool](text-diff.html)** — compare two text blocks and highlight added and removed content

### Web development

- **[Favicon Generator](favicon-generator.html)** — generate favicons in multiple sizes and formats including SVG, ICO, Apple Touch Icons, and Android icons

### Web privacy & security

- **[Browser Fingerprint Viewer](browser-fingerprint.html)** — view browser fingerprint data that websites can collect including canvas fingerprinting, WebGL info, audio context, detected fonts, and device characteristics
- **[Cookie & Storage Analysis](cookie-storage-analysis.html)** — examine all data websites can store on your device including cookies, localStorage, sessionStorage, IndexedDB, cache storage, and service workers with detailed analysis

## Acknowledgement

This set of tools has been developed using a range of agentic coding tools. This collection was inspired by [Simon Willison's](https://simonwillison.net/) experiment in prompt-driven development, using LLMs to develop his own set of standalone HTML + Javascript tools. Simon's code lives on GitHub in [simonw/tools](https://github.com/simonw/tools) and many of his tools used the Claude custom instructions [described here](https://simonwillison.net/2024/Dec/19/one-shot-python-tools/#custom-instructions).
