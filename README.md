# DataVision Analytics — Tableau Dashboard App

A professional Flask web app to showcase your Tableau Public dashboards and stories.

## Setup

```bash
pip install -r requirements.txt
python app.py
```
Then open http://localhost:5000

## 🔑 Connect Your Tableau Pages

Open `app.py` and update the `TABLEAU` dictionary with **your actual Tableau Public URLs**:

```python
TABLEAU = {
    "dashboard1": {
        "name": "Your Dashboard 1 Name",
        "url": "https://public.tableau.com/views/YourWorkbook/YourSheet",
        ...
    },
    "dashboard2": {
        "name": "Your Dashboard 2 Name",
        "url": "https://public.tableau.com/views/YourWorkbook2/YourSheet2",
        ...
    },
    "story": {
        "name": "Your Story Name",
        "url": "https://public.tableau.com/views/YourStoryWorkbook/YourStory",
        ...
    }
}
```

### How to get your Tableau Public URL:
1. Go to your Tableau Public profile
2. Click on the viz you want to embed
3. Click **Share** → copy the **Link** (not the embed code)
4. It looks like: `https://public.tableau.com/views/WorkbookName/SheetName`
5. Paste that as the `"url"` value in `app.py`

## Project Structure

```
tableau_app/
├── app.py              ← Flask routes + Tableau URL config
├── requirements.txt
├── templates/
│   ├── base.html       ← Header, footer, shared layout
│   ├── home.html       ← Landing page
│   ├── dashboards.html ← Two embedded dashboards
│   └── story.html      ← Embedded story
└── static/
    ├── css/style.css
    └── js/main.js
```
