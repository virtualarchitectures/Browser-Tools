# AGENTS.md

## Guidelines for AI Agents Working on Browser-Tools

This document provides instructions for AI coding assistants (Claude, ChatGPT, Gemini, Cursor, etc.) working on this repository.

## Core Principles

### 1. Never Use React in Artifacts

**CRITICAL REQUIREMENT:** Always use plain HTML, vanilla JavaScript, and CSS with minimal dependencies.

- ❌ **DO NOT** use React, Vue, Angular, or any other frontend framework
- ❌ **DO NOT** use JSX or any transpilation step
- ❌ **DO NOT** introduce build tools (webpack, vite, rollup, etc.)
- ✅ **DO** use plain HTML5, vanilla JavaScript (ES6+), and CSS3
- ✅ **DO** keep tools as single self-contained HTML files when possible
- ✅ **DO** prioritize browser-native APIs and features

### 2. No Server-Side Processing

All tools must run entirely in the browser:

- ✅ All processing happens client-side using JavaScript
- ✅ All data stays in the user's browser
- ✅ Files are processed using FileReader API, Web APIs, etc.
- ❌ No backend services, APIs, or server endpoints (except for well-known, stable third-party services when absolutely necessary)

## Technical Guidelines

### File Structure

Each tool should typically be:
- A single, self-contained HTML file
- Include all CSS in a `<style>` tag
- Include all JavaScript in a `<script>` tag
- Clearly organized with comments separating sections

### Code Style

**HTML:**
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tool Name</title>
    <style>
      /* CSS here */
    </style>
  </head>
  <body>
    <!-- Content here -->
    <script>
      // JavaScript here
    </script>
  </body>
</html>
```

**JavaScript:**
- Use modern ES6+ syntax (const/let, arrow functions, async/await, etc.)
- Use browser-native APIs (FileReader, Blob, Canvas, etc.)
- Prefer functional approaches where appropriate
- Add clear comments explaining complex logic
- Use descriptive variable and function names

**CSS:**
- Use system fonts for performance and consistency
- Responsive design with mobile-first approach
- Simple, clean styling
- Use CSS Grid and Flexbox for layouts

### Dependencies

**Minimal External Dependencies:**
- Only include external libraries when absolutely necessary
- Prefer CDN links over npm packages
- Document why each dependency is needed
- Examples of acceptable dependencies:
  - Specialized libraries (e.g., exif-js for EXIF data, jsdiff for text comparison)
  - Mapping libraries (e.g., Leaflet for GeoJSON visualization)
  - PDF.js for PDF processing

**Unacceptable Dependencies:**
- React, Vue, Angular, Svelte, or any framework
- jQuery (use vanilla JavaScript instead)
- Bootstrap (write custom CSS instead)
- Lodash/Underscore (use native JavaScript methods)

### Browser Compatibility

- Target modern evergreen browsers (Chrome, Firefox, Safari, Edge)
- Use standard Web APIs that have broad support
- Test features using MDN compatibility tables
- Provide graceful degradation or clear error messages for unsupported features

### User Experience

**Input Handling:**
- Support drag-and-drop for file inputs
- Provide clear feedback during processing
- Show loading states for long operations
- Handle errors gracefully with user-friendly messages

**Output:**
- Display results clearly and accessibly
- Provide download capabilities where appropriate
- Show previews of data when helpful
- Include copy-to-clipboard functionality when relevant

**Accessibility:**
- Use semantic HTML elements
- Include appropriate ARIA labels
- Ensure keyboard navigation works
- Use sufficient color contrast

## Development Workflow

### Creating a New Tool

1. **Single File**: Create a new `.html` file in the root directory
2. **Naming**: Use kebab-case (e.g., `my-new-tool.html`)
3. **Self-Contained**: Include all HTML, CSS, and JavaScript in one file
4. **Test Locally**: Open in browser directly (no build step needed)
5. **Update Index**: Add the tool to `index.html` in the appropriate category
6. **Update README**: Add a description in `README.md` under "Available Tools"

### Modifying Existing Tools

1. **Understand First**: Read the entire file to understand its structure
2. **Maintain Style**: Follow the existing code style and patterns
3. **Test Thoroughly**: Verify all functionality still works
4. **Document Changes**: Add comments explaining significant modifications

### Code Organization Within a File

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tool Name</title>
    <style>
      /* =========================
         CSS Styles
         ========================= */
      
      /* Reset and base styles */
      /* Layout */
      /* Components */
      /* Utilities */
    </style>
  </head>
  <body>
    <!-- =========================
         HTML Structure
         ========================= -->
    
    <script>
      /* =========================
         JavaScript
         ========================= */
      
      // State variables
      // Utility functions
      // Event handlers
      // Initialization
    </script>
  </body>
</html>
```

## Common Patterns

### File Upload

```javascript
// Drag and drop
dropZone.addEventListener('drop', (e) => {
  e.preventDefault();
  const files = e.dataTransfer.files;
  handleFile(files[0]);
});

// File input
fileInput.addEventListener('change', (e) => {
  handleFile(e.target.files[0]);
});

// Reading files
function handleFile(file) {
  const reader = new FileReader();
  reader.onload = (e) => {
    const content = e.target.result;
    processContent(content);
  };
  reader.readAsText(file);
}
```

### Download Files

```javascript
function downloadFile(content, filename, mimeType) {
  const blob = new Blob([content], { type: mimeType });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = filename;
  a.click();
  URL.revokeObjectURL(url);
}
```

### Error Handling

```javascript
try {
  // Risky operation
  processData(data);
} catch (error) {
  console.error('Error:', error);
  showError('Failed to process data: ' + error.message);
}

function showError(message) {
  const errorDiv = document.getElementById('error');
  errorDiv.textContent = message;
  errorDiv.style.display = 'block';
}
```

## Testing Checklist

Before considering a tool complete:

- [ ] Works in Chrome, Firefox, Safari, and Edge
- [ ] No console errors or warnings
- [ ] Handles edge cases (empty files, large files, malformed data)
- [ ] Provides clear error messages
- [ ] Responsive on mobile devices
- [ ] Accessible via keyboard navigation
- [ ] Drag-and-drop works correctly
- [ ] Download/copy functionality works
- [ ] No external dependencies unless documented and necessary
- [ ] Code is well-commented
- [ ] Added to index.html
- [ ] Documented in README.md

## Examples

Good examples from this repository:
- `text-diff.html` - Clean, focused, single-purpose tool
- `csv-to-json.html` - Good file handling and preview functionality
- `pixel-coords.html` - Simple, effective use of Canvas API

## Questions?

When in doubt:
1. **Keep it simple** - The simplest solution is usually the best
2. **No frameworks** - Vanilla JS can do everything you need
3. **Self-contained** - One file, no build step
4. **User-focused** - Prioritize clarity and usability
