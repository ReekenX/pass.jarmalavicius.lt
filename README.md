# Passphrase Generator

A simple, privacy-focused passphrase generator that creates memorable yet secure passwords using random common English words.

**Live**: https://pass.jarmalavicius.lt/ (press `SPACE` to toggle password length)

## Privacy First

- **No analytics** - zero tracking scripts or cookies
- **No backend** - everything runs entirely in your browser
- **No data collection** - your generated passwords never leave your device
- **No external requests** - the page works completely offline after loading

## How It Works

The generator creates passphrases by:

1. Randomly selecting words from a dictionary of ~7,776 common English words
2. Joining words with commas as separators
3. Capitalizing the first letter
4. Appending the total password length at the end

Example output: `Bamboo,aircraft,horizon,deeply,73`

## Features

- **No server-side processing** - all password generation happens in your browser
- **Three length modes** - toggle with SPACE key:
  - Short: 20-30 characters
  - Medium: 60-70 characters (default)
  - Long: 120-130 characters
- **Instant regeneration** - press SPACE to cycle through length modes and generate a new password

## Usage

1. Visit the page - a password is generated automatically
2. Press **SPACE** to toggle between length modes and generate a new password
3. Copy the displayed password

## Running Locally

### Option 1: Open directly
Simply open `index.html` in your browser.

### Option 2: Docker
```bash
docker-compose up -d
```
The site will be available at http://localhost:8080

## Project Structure

```
.
├── index.html          # Single-file application (HTML + CSS + JS + word list)
├── docker-compose.yml  # Docker configuration for nginx hosting
├── LICENSE             # GPL-3.0 license
└── README.md
```

## Security Note

This generator uses `Math.random()` for word selection, which is not cryptographically secure. For high-security applications, consider using a generator with `crypto.getRandomValues()`. However, for most use cases, the entropy from 7,776 words provides adequate security - a 6-word passphrase has approximately 77 bits of entropy.

## License

GPL-3.0
