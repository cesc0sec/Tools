# Tools Collection

This repository is for small utility tools.

## CSRF Form Generator (csrf_formgen.py)

A Python utility to convert raw HTTP POST requests into HTML forms for CSRF testing.
#### Features

    Supports application/x-www-form-urlencoded and multipart/form-data POST requests.
    Converts multipart data into hidden HTML inputs.
    Reads raw HTTP request from a file or standard input.
    Output filename customizable (default: csrf.html).

#### Usage

```bash
python3 csrf_formgen.py -f path/to/request.txt -o output.html
```

## Race Condition Tester (racecon.py)

This script is designed to test for race condition vulnerabilities by sending multiple concurrent requests to a target endpoint.

#### Features
    
    Send requests in parallel using threads.
    Customize:
        URL
        HTTP method (GET, POST, PUT, etc.)
        Headers
        Number of threads

#### Requirements

    Python 3.7+
    Dependencies listed in requirements.txt

Install with:

pip install requirements.txt

#### Usage

python racecon.py [-h] -u URL [-X METHOD] [-H HEADER] [-t THREADS]
Example

```bash
python racecon.py -u https://example.com/api/claim -X POST -H "Content-Type: application/json" -H "Cookie: session=abc123" -t 100
```
