# Virtual Registrar Queue System

The Virtual Registrar Queue System is a proposed web application for the MSU-IIT University Registrar that allows students to join a walk-in queue remotely and monitor their queue progress while authorized staff manage the queue. 

To run the application locally, activate the Python virtual environment, install the dependencies using pip install -r requirements.txt, and execute flask --app app run --debug. Then open http://127.0.0.1:5000 in your browser.

## Project structure

```
my-app/
├── app.py              # creates the app and defines routes
├── requirements.txt    # packages to rebuild the environment
├── .gitignore          # keeps .venv, caches and secrets out of Git
├── .venv/              # your virtual environment (not committed)
├── templates/          # Jinja2 HTML files for render_template()
│   ├── base.html       # shared layout
│   ├── index.html      # home page
│   └── ticket.html     # page for /queue/<ticket_id>
└── static/             # served at /static/...
    ├── css/style.css
    └── js/main.js
```


## 1. Set up the Python environment

```bash
# create (once per project)
python -m venv .venv

# activate (every new terminal)
.venv\Scripts\activate          # Windows
source .venv/bin/activate       # macOS/Linux

# install the packages
pip install -r requirements.txt
```

Your prompt shows `(.venv)` when the environment is active. Some systems use `python3` or `py` instead of `python`.
If PowerShell blocks the activate script, run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` once, or use Command Prompt.

If you add more packages later, record them with:

```bash
pip freeze > requirements.txt
```

## 2. Run the app

```bash
flask --app app run --debug
```

Open http://127.0.0.1:5000. With `--debug`, the server reloads every time you save a file. Never use debug mode in production.


### Everyday loop

```bash
git pull origin main     # before you start working
git status
git add <file>
git commit -m "Add join-queue form"
git push origin main     # when you have commits to share
```

