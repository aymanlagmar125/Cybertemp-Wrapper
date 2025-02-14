<div align="center">
  <h2 align="center">CyberTemp API Client</h2>
  <p align="center">
    A Python client for interacting with the CyberTemp temporary email service API.
    <br />
    <br />
    <a href="https://cybertemp.xyz">🌐 Website</a>
    ·
    <a href="#-changelog">📜 ChangeLog</a>
    ·
    <a href="https://github.com/sexfrance/cybertemp-wrapper/issues">⚠️ Report Bug</a>
  </p>
</div>

---

### ⚙️ Installation

```bash
pip install cybertemp
```

### 🚀 Quick Start

```python
from cybertemp.cybertemp import CyberTemp

# Initialize (free tier)
client = CyberTemp()

# Or with API key (premium)
client = CyberTemp(api_key="your_api_key_here")

# Get available domains
domains = client.get_domains()

# Check mailbox
emails = client.get_email_content("test@cybertemp.xyz")
```

You can purchase an api key here: https://cybertemp.xyz/pricing

### 📚 API Reference

#### Initialization
```python
client = CyberTemp(
    debug=True,           # Enable debug logging
    api_key=None,         # Optional API key for premium features
)
```

#### Available Methods

1. **Get Email Content**
```python
emails = client.get_email_content("test@cybertemp.xyz")
```

2. **Get Email by ID**
```python
email = client.get_email_content_by_id("email_id_here")
```

3. **Get Available Domains**
```python
domains = client.get_domains()
```

4. **Search Email by Subject**
```python
mail_id = client.get_mail_by_subject(
    email="test@cybertemp.xyz",
    subject_contains="Verification",
    max_attempts=10
)
```

5. **Extract URL from Email**
```python
url = client.extract_url_from_message(
    email="test@cybertemp.xyz",
    subject_contains="Verification",
    url_pattern=r'https://[^\s<>"]+'
)
```

6. **Check API Balance** (Premium)
```python
balance = client.get_balance()
```

### 💳 Premium Features

- No rate limiting
- API key support
- Credit system
- Priority support

### ⚠️ Rate Limits

- Free tier: 1-second delay between requests
- Premium tier: No delays, pay-per-use

### 📜 ChangeLog

```diff
v1.0.0 ⋮ 202-02-14
! Initial release

```

<p align="center">
  <img src="https://img.shields.io/github/license/sexfrance/Cybertemp-Wrapper.svg?style=for-the-badge&labelColor=black&color=f429ff&logo=IOTA"/>
  <img src="https://img.shields.io/github/stars/sexfrance/Cybertemp-Wrapper.svg?style=for-the-badge&labelColor=black&color=f429ff&logo=IOTA"/>
  <img src="https://img.shields.io/github/languages/top/sexfrance/Cybertemp-Wrapper.svg?style=for-the-badge&labelColor=black&color=f429ff&logo=python"/>
  <img alt="PyPI - Downloads" src="https://img.shields.io/pypi/dm/Cybertemp.svg?style=for-the-badge&labelColor=black&color=f429ff&logo=IOTA">
</p>

