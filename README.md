# Browser Tools

A collection of browser-based HTML+JavaScript tools for various tasks. These tools are prototypes, not products. They have been developed quickly and iteratively using LLMs to test the afforances and limitations of agentic coding. Each tool has been tailored to my own practical needs. At the same time they are also intended to provide genuine utility and value for others.

Some tools require external dependencies which are loaded from trusted CDNs. All tools run entirely in your browser with no server-side processing.

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
- **[Table Editor](table-editor.html)** — create tables or load existing CSV files for editing, export to CSV, JSON, or JSON Lines format

### Digital Forensics

- **[Email Header Analysis](email-header-analysis.html)** — analyse and highlight email headers with syntax highlighting for IPs, emails, and URLs

### Documents and Text

- **[OCR Reader](ocr-reader.html)** — extract text from images and PDF files using optical character recognition with side-by-side preview
- **[PDF Metadata Viewer](pdf-metadata.html)** — extract and view PDF metadata including title, author, dates, permissions, and security settings
- **[PDF Cropper](pdf-cropper.html)** — remove headers, footers, page numbers, and margins from PDF documents by dragging bars to frame the content area you want to keep
- **[PDF to Images](pdf-to-images.html)** — extract high-quality images of pages from PDF documents with adjustable DPI and format options (PNG, JPEG, WebP)
- **[PDF Editor](pdf-editor.html)** — remove pages from PDF documents by selecting page ranges or clicking page previews with visual page thumbnails
- **[Presentation Annotator](annotated-presentation.html)** — add alt text and markdown annotations to presentation slide images with template-based export and live preview
- **[Text Chunking](text-chunking.html)** — split text documents into manageable chunks using multiple strategies (character count, word count, sentence-based, paragraph-based, recursive split, sliding window) with configurable overlap and export to CSV
- **[Text Diff](text-diff.html)** — compare two text blocks and highlight added and removed content
- **[Text Tools](text-tools.html)** — text manipulation toolkit with case transformation, sorting, whitespace cleaning, encoding/decoding (Base64, URL), find & replace, and text tokenization

### Image

- **[EXIF Data Viewer](exif-viewer.html)** — extract and view EXIF metadata from photos including camera settings, GPS location, and timestamps
- **[Image Background Removal](image-bg-removal.html)** — remove image backgrounds using a magic wand flood-fill tool with adjustable tolerance and edge feathering, then download as transparent PNG
- **[Image Crop Tool](image-crop.html)** — crop images with interactive selection, aspect ratio presets, and precise dimension controls
- **[Image Resize Tool](image-resize.html)** — resize images by percentage or pixels with precise scale factor control for copying scale factor to other images
- **[Image Rotate Tool](image-rotate.html)** — rotate images by any angle with fine control, flip horizontally or vertically
- **[Pixel Coordinates](pixel-coords.html)** — click on images to capture and record pixel coordinates

### Media

- **[Multi-Webcam Viewer](webcam-viewer.html)** — view multiple webcam feeds simultaneously with support for YouTube embeds, direct video streams (MP4, M3U8, HLS), and iframe-compatible sources
- **[Scene Detection Tool](scene-detection.html)** — automatically detect scene changes in videos using frame analysis with adjustable sensitivity, minimum scene duration, and sample rate controls
- **[Transcription Tool](transcribe.html)** — transcribe audio and video files with keyboard shortcuts, timestamps, and speed control

### Network Data

- **[Network Diagram Builder](network-diagram.html)** — create network diagrams interactively by drawing nodes and edges with custom properties, export to Neo4j Cypher, NetworkX Python, GEXF, and GraphML formats

### Maps and Spatial Data

- **[Feature Service Viewer](feature-service-viewer.html)** — load and visualize ArcGIS Feature Services and MapServer layers on an interactive map
- **[GeoJSON Editor](geojson-editor.html)** — draw points, polygons, and lines on an interactive map, add custom properties, and export as GeoJSON
- **[GeoJSON Viewer](geojson-viewer.html)** — visualize and explore GeoJSON files on an interactive map

### Natural Language Processing (NLP)

- **[AI Writing Detector](ai-writing-detector.html)** — analyze text for patterns commonly associated with LLM-generated content including AI vocabulary, significance claims, promotional language, weasel words, structural patterns, punctuation analysis, and LLM artifacts
- **[Concept Analysis](concept-analysis.html)** — extract sentences containing specific concepts or phrases from text and automatically categorize results as definitions, distinctions, or explanations using NLP and RegEx
- **[Named Entity Recognition](named-entity-recognition.html)** — extract and identify named entities from text including people, places and organisations using natural language processing
- **[Sentiment Analysis](sentiment-analysis.html)** — analyze sentiment in CSV text columns using AFINN lexicon with configurable metrics (score, comparative, classification, word counts, tokens) and summary statistics
- **[Word Frequency Counter](word-frequency.html)** — analyze word frequency, discover common phrases with n-grams (bigrams, trigrams, 4-grams, 5-grams), and get detailed text statistics with customisable stop word filtering

### OSINT

- **[Article Access Tool](article-access.html)** — locate accessible versions of news articles via the Internet Archive (Wayback Machine) or optional proxy extraction with Mozilla Readability
- **[Identifier Extractor](identifier-extractor.html)** — extract and analyse URLs, email addresses, IPv4/IPv6 addresses, phone numbers, and MAC addresses from text with filtering, sorting, and export options

### Software Development

- **[GitHub Commits Viewer](github-commits.html)** — view and export commit history from GitHub repositories with support for CSV, JSON, and Markdown exports
- **[Localhost Port Scanner](localhost-port-scanner.html)** — scan ports on your local machine to detect running services, Docker containers, and development servers with preset scans for common ports and custom range options

### Web Development

- **[Favicon Generator](favicon-generator.html)** — generate favicons in multiple sizes and formats including SVG, ICO, Apple Touch Icons, and Android icons
- **[Robots.txt Checker](robots-txt-checker.html)** — fetch and parse robots.txt files from websites and check whether specific URLs or paths are allowed or disallowed for different web crawlers

### Web Privacy & Security

- **[Browser Fingerprint Viewer](browser-fingerprint.html)** — view browser fingerprint data that websites can collect including canvas fingerprinting, WebGL info, audio context, detected fonts, and device characteristics
- **[Cookie & Storage Analysis](cookie-storage-analysis.html)** — examine all data websites can store on your device including cookies, localStorage, sessionStorage, IndexedDB, cache storage, and service workers with detailed analysis

## Acknowledgements

Development of this collection was inspired by Simon Willison's experiments in prompt-driven development. Simon's collection can be found at [https://tools.simonwillison.net/](https://tools.simonwillison.net/), and his code can be found on GitHub in [simonw/tools](https://github.com/simonw/tools). Simon also generously discusses both the [Claude custom instructions](https://simonwillison.net/2024/Dec/19/one-shot-python-tools/#custom-instructions) and [general patterns](https://simonwillison.net/2025/Dec/10/html-tools/) he uses for developing these tools on his blog.

The majority of tools in my collection [virtualarchitectures/Browser-Tools](https://github.com/virtualarchitectures/Browser-Tools) have been developed using Anthropic's Claude running within the Zed agentic IDE. I've also used a combination of Claude, ChatGPT and Google Gemini within Continue.Dev in VS Code for more focused edits and refinement. In each case the LLM has been used to tailor the tool to meet my own practical needs. This practice is in broad alignment with approaches discussed elsewhere under the headings of [malleable software](https://www.inkandswitch.com/essay/malleable-software/) and [resonant computing](https://resonantcomputing.org/). More generally, my personal preference in the use of LLMs is toward local development on my own machine using open models in [Ollama](https://ollama.com/).
