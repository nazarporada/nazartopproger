# File Uploader Package

This is a simple Node.js package for handling file uploads using Express and Multer.

## Installation

Install the package via npm:

```bash
npm install express multer file-uploader
```

## Usage

1. Require the `file-uploader` package in your Node.js application:

```javascript
const express = require('express');
const fileUploader = require('file-uploader');
```

2. Initialize an Express app:

```javascript
const app = express();
```

3. Define a route for handling file uploads:

```javascript
app.post('/upload', fileUploader.upload.single('file'), (req, res) => {
  res.json({ message: 'File uploaded successfully', filename: req.file.filename });
});
```

4. Start the server:

```javascript
const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
```

## Configuration

You can configure the destination directory and filename format for uploaded files by modifying the `storage` object in the `index.js` file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
