# www - GitHub Pages Site

Public repository for hosting GitHub Pages content.

## 🌐 Live Site

**URL**: https://tkdpython.github.io/www/

## 📊 Health Metrics

This repository hosts health metrics data from Google Fit:

- **Dashboard**: https://tkdpython.github.io/www/
- **JSON API**: https://tkdpython.github.io/www/health_metrics.json

### Data Updates

The `health_metrics.json` file is automatically updated by the [healthpages](https://github.com/tkdpython/healthpages) repository workflow:
- **Schedule**: Daily at 06:00 UTC
- **Source**: Private healthpages repository workflow
- **Method**: Workflow pushes JSON to this public repo

## 📁 Files

- **index.html** - Interactive health metrics dashboard
- **health_metrics.json** - Auto-generated Google Fit data (updated by workflow)

## 🔧 Setup

1. Ensure this repository is **public**
2. Enable GitHub Pages:
   - Go to **Settings** → **Pages**
   - Source: **Deploy from a branch**
   - Branch: **main** / **root**
   - Click **Save**

3. Configure the healthpages workflow to push to this repo

## 📖 Usage

Access the JSON data programmatically:

```javascript
fetch('https://tkdpython.github.io/www/health_metrics.json')
  .then(response => response.json())
  .then(data => {
    console.log('Steps:', data.metrics.steps);
    console.log('Calories:', data.metrics.calories);
  });
```

```python
import requests
response = requests.get('https://tkdpython.github.io/www/health_metrics.json')
data = response.json()
print(f"Last updated: {data['last_updated']}")
```

## 🔐 Privacy Note

This is a **public** repository. The health metrics data published here is publicly accessible.
Sensitive credentials and private data remain in the private healthpages repository.
