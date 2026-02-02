# Voilà Test - Deployment to Render.com

## Files Needed:
1. `test_voila.ipynb` - Your computational essay notebook
2. `requirements.txt` - Python dependencies

## Render.com Setup:

### Create New Web Service:
1. Connect your GitHub repo (or use "Deploy from Git URL")
2. Settings:
   - **Name**: `voila-test` (or whatever you want)
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `voila test_voila.ipynb --port=$PORT --no-browser --Voila.ip=0.0.0.0`
   - **Instance Type**: Free tier to test

### Custom Domain:
After it deploys, add custom domain: `ou-essay.nippofin.com`

## Local Testing (Optional):
```bash
pip install -r requirements.txt
voila test_voila.ipynb --port=8866
# Visit http://localhost:8866
```

## For Your Actual OU Essay:
1. Replace `test_voila.ipynb` with `ouVarMean.ipynb`
2. Add LaTeX theory sections as markdown cells at the top
3. Update requirements.txt if you need additional packages
4. Deploy!

## What Visitors Will See:
- Clean essay with markdown and equations
- Interactive plots (no code cells unless you want to show them)
- Professional presentation

## Options:
- To SHOW code: `voila notebook.ipynb --strip_sources=False`
- To HIDE code: default behavior (code hidden, only outputs shown)
