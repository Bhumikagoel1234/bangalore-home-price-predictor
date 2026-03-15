# Deploy to Render - Step by Step Guide

## Prerequisites
- GitHub account
- Render account (free - sign up at render.com)

## Step 1: Push to GitHub

1. Go to GitHub.com and create a new repository
2. Name it: `bangalore-home-price-predictor`
3. Don't initialize with README (we already have files)

4. In your project folder, open Command Prompt and run:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bangalore-home-price-predictor.git
git push -u origin main
```

## Step 2: Deploy on Render

1. Go to https://render.com and sign up/login
2. Click "New +" → "Web Service"
3. Connect your GitHub account
4. Select your repository: `bangalore-home-price-predictor`
5. Configure:
   - **Name**: bangalore-home-price-predictor
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn app:app`
   - **Plan**: Free

6. Click "Create Web Service"

## Step 3: Wait for Deployment

- Render will build and deploy (takes 5-10 minutes)
- You'll get a URL like: `https://bangalore-home-price-predictor.onrender.com`
- This URL works on any device (phone, tablet, computer)

## Important Notes

⚠️ **Free Tier Limitations:**
- App sleeps after 15 minutes of inactivity
- First load after sleep takes 30-60 seconds
- 750 hours/month free

## Troubleshooting

If deployment fails:
1. Check build logs in Render dashboard
2. Ensure all files are committed to GitHub
3. Verify requirements.txt has correct versions

## Access on Phone

Once deployed:
1. Open any browser on your phone
2. Go to your Render URL
3. Website is fully responsive and works on mobile!

## Alternative: If You Don't Want GitHub

You can also:
1. Upload files directly to Render (manual deploy)
2. Use Render's GitHub integration without making repo public

---

**Your project will be live and accessible from anywhere! 🚀**
