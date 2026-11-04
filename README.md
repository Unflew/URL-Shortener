# 🔗 URL Shortener

A simple URL Shortener built with Python using the built-in `http.server` module.

This project allows users to convert long URLs into short links and automatically redirect visitors to the original URLs.

## 🚀 Features

- Shortens URLs using MD5 hashing.
- Generates unique 8-character URL identifiers.
- Stores URL mappings in memory.
- Redirects users to original URLs using HTTP 307.
- Handles invalid and non-existent URLs.
- Uses Python's built-in libraries.

## 🛠️ Technologies

- Python 3
- `http.server`
- `hashlib`
- `typing`

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Navigate to the project directory:

```bash
cd YOUR_REPOSITORY
```

No additional dependencies are required.

## ▶️ Usage

Start the server:

```bash
python main.py
```

The server will start at:

```text
http://127.0.0.1:8080
```

### 1. Create a short URL

Send a POST request with the original URL:

```bash
curl -X POST http://127.0.0.1:8080/ \
     -d "https://google.com"
```

The server will return a shortened URL, for example:

```text
http://127.0.0.1:8080/a1b2c3d4
```

### 2. Open the shortened URL

Open the generated link in your browser or use:

```bash
curl -i http://127.0.0.1:8080/a1b2c3d4
```

The server will redirect you to the original URL.

## 📁 Project Structure

```text
URL-Shortener/
│
├── main.py
└── README.md
```

## ⚠️ Limitations

- URL mappings are stored in memory and disappear when the server stops.
- The server runs locally by default (`127.0.0.1`).
- MD5 hashing may produce collisions.
- URLs are not validated before being stored.
- The built-in HTTP server is intended for development and educational purposes, not production use.

## 🎯 Purpose

This project was created for educational purposes to demonstrate:

- Basic HTTP server development in Python.
- Handling GET and POST requests.
- URL shortening logic.
- Hash generation using MD5.
- HTTP redirection.

## 📄 License

This project is available under the MIT License.
