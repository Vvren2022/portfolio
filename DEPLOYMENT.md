# Portfolio Deployment Guide

This guide will help you deploy your portfolio website to get a public URL like `https://yourname.netlify.app`

## Option 1: Netlify (Recommended - Easiest)

Netlify offers free hosting with a custom subdomain for static websites.

### Steps:

1. **Create a GitHub Repository**
   - Go to [GitHub](https://github.com) and sign in
   - Click "New Repository"
   - Name it `portfolio` or `my-portfolio`
   - Make it Public
   - Create the repository

2. **Upload Your Portfolio Files to GitHub**
   - Open your terminal in the `portfolio_site` folder
   - Run these commands:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git push -u origin main
   ```
   (Replace `YOUR_USERNAME` with your GitHub username)

3. **Deploy to Netlify**
   - Go to [Netlify](https://www.netlify.com/)
   - Click "Sign up" and sign up with your GitHub account
   - Once logged in, click "Add new site" → "Import an existing project"
   - Choose "GitHub"
   - Select your `portfolio` repository
   - Click "Deploy site"

4. **Customize Your Domain**
   - After deployment, go to "Site settings"
   - Click "Change site name"
   - Enter your desired name (e.g., `virenvaviya`)
   - Your site will be available at `https://virenvaviya.netlify.app`

5. **Configure EmailJS**
   - Go to [EmailJS](https://www.emailjs.com/)
   - Sign up for a free account
   - Create an email service (Gmail recommended)
   - Create an email template
   - Get your Public Key, Service ID, and Template ID
   - Update `script.js` with these values

## Option 2: Vercel

Similar to Netlify, also offers free hosting.

### Steps:

1. Create GitHub repository (same as above)
2. Go to [Vercel](https://vercel.com/)
3. Sign up with GitHub
4. Click "Add New" → "Project"
5. Import your repository
6. Deploy

Your domain will be: `https://portfolio-yourname.vercel.app`

## Option 3: GitHub Pages

Free hosting directly from your GitHub repository.

### Steps:

1. Create a repository named `YOUR_USERNAME.github.io`
2. Upload your portfolio files
3. Go to repository Settings → Pages
4. Select "main" branch as source
5. Your site will be at `https://YOUR_USERNAME.github.io`

## Recommended: Use Netlify

**Why Netlify?**
- ✅ Easiest to set up
- ✅ Automatic deployments when you update code
- ✅ Free custom subdomain (e.g., `virenvaviya.netlify.app`)
- ✅ Free SSL certificate (https)
- ✅ Fast content delivery network (CDN)
- ✅ Can add custom domain later (optional, paid)

## After Deployment

1. **Update LinkedIn**
   - Go to your LinkedIn profile
   - Click "Add profile section" → "Featured"
   - Add your portfolio link

2. **Test EmailJS**
   - Fill out the contact form on your live site
   - Check if you receive the email

3. **Share Your Portfolio**
   - Add to your resume
   - Share on social media
   - Include in job applications

## Need Help?

If you encounter any issues during deployment, let me know and I'll help you troubleshoot!
