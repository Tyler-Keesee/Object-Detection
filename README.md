# Object Detection

An experimental browser-based object-detection demo using local JavaScript assets.

## Windows 11: exact setup (PowerShell)

Install Git and Python 3 (only needed to serve the static files). Run **one command at a time**:

```powershell
git clone https://github.com/Tyler-Keesee/Object-Detection.git
```

```powershell
Set-Location .\Object-Detection
```

```powershell
python -m http.server 8000
```

With PowerShell still running, open **http://localhost:8000/** in Edge. Press **Ctrl+C** to shut down the local server.

No `pip install`, `venv`, `npm ci`, or `download-models.ps1` step is needed to start serving the included files; `download-models.ps1` is currently empty. This static site includes local model-related JavaScript and labels; whether TensorFlow models initialize successfully still needs testing in the browser.

**Verification:** A successful HTTP response only proves the site loads, not that object detection runs. Allow camera access only when you intend to test it, and inspect the browser Console/Network errors if detection does not start.
