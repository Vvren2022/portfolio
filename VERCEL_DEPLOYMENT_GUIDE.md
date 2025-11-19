# Complete Vercel Deployment Guide
## Get Your Portfolio Live at https://virenvaviya.vercel.app

Follow these steps to deploy your portfolio website and get a free domain.

---

## Part 1: Setup GitHub (5 minutes)

### Step 1: Create GitHub Account
1. Go to https://github.com/signup
2. Enter your email: `vrenvaviya2022@gmail.com`
3. Create a password
4. Choose a username (e.g., `Vvren2022` - you already have this!)
5. Verify your email

### Step 2: Create New Repository
1. After signing in, click the **"+"** icon (top right)
2. Click **"New repository"**
3. Fill in:
   - **Repository name**: `portfolio`
   - **Description**: `My AI/ML Portfolio Website`
   - **Public** (selected)
   - ❌ **Don't** check "Add a README"
4. Click **"Create repository"**

### Step 3: Upload Your Portfolio Files

**Option A: Using Git Commands (Recommended)**

Open PowerShell in your `portfolio_site` folder and run:

```powershell
# Navigate to your portfolio folder
cd c:\Users\piyus\.gemini\antigravity\scratch\django_crud\portfolio_site

# Initialize git
git init

# Add all files
git add .

# Commit files
git commit -m "Initial portfolio commit"

# Rename branch to main
git branch -M main

# Add remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git

# Push to GitHub
git push -u origin main
```

**Option B: Upload via Web Interface (Easier)**

1. On the repository page, click **"uploading an existing file"**
2. Drag and drop ALL files from your `portfolio_site` folder:
   - `index.html`
   - `style.css`
   - `script.js`
   - `README.md`
   - `DEPLOYMENT.md`
3. Click **"Commit changes"**

---

## Part 2: Deploy to Vercel (3 minutes)

### Step 1: Sign Up for Vercel
1. Go to https://vercel.com/signup
2. Click **"Continue with GitHub"**
3. Authorize Vercel to access your GitHub
4. Complete the signup process

### Step 2: Create New Project
1. After signing in, click **"Add New"** → **"Project"**
2. You'll see a list of your GitHub repositories
3. Find **"portfolio"** and click **"Import"**

### Step 3: Configure Project
1. **Framework Preset**: Leave as "Other"
2. **Root Directory**: Leave as `./`
3. Click **"Deploy"**

### Step 4: Wait for Deployment
- Vercel will build and deploy your site (~30 seconds)
- You'll see a preview of your live site
- Your temporary URL will be something like:
  `https://portfolio-abc123.vercel.app`

### Step 5: Customize Your Domain
1. Go to **"Settings"** tab (top menu)
2. Click **"Domains"** (left sidebar)
3. In the "Domains" section, you'll see your current domain
4. Click **"Edit"** or type in the input field:
   ```
   virenvaviya.vercel.app
   ```
5. Click **"Add"**
6. If the name is available, it will be assigned to your project

**🎉 Your portfolio is now live at: `https://virenvaviya.vercel.app`**

---

## Part 3: Configure EmailJS (10 minutes)

To make your contact form work, you need to set up EmailJS.

### Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Click **"Sign Up"**
3. Use your email: `vrenvaviya2022@gmail.com`
4. Verify your email

### Step 2: Add Email Service
1. In EmailJS dashboard, click **"Email Services"**
2. Click **"Add New Service"**
3. Select **"Gmail"**
4. Click **"Connect Account"**
5. Sign in with your Gmail account
6. Allow EmailJS to access your Gmail
7. **Note down your Service ID** (e.g., `service_abc123`)

### Step 3: Create Email Template
1. Click **"Email Templates"**
2. Click **"Create New Template"**
3. Replace the template with:

**Subject:**
```
New Contact from Portfolio: {{user_name}}
```

**Content:**
```
You have a new message from your portfolio website!

Name: {{user_name}}
Email: {{user_email}}

Message:
{{message}}

---
This email was sent from your portfolio contact form.
```

4. Click **"Save"**
5. **Note down your Template ID** (e.g., `template_xyz789`)

### Step 4: Get Your Public Key
1. Click **"Account"** (top right)
2. Go to **"API Keys"** tab
3. **Note down your Public Key** (e.g., `YOUR_PUBLIC_KEY`)

### Step 5: Update Your Code
1. Open `script.js` in your portfolio folder
2. Find these lines (around line 128):
   ```javascript
   emailjs.init('YOUR_PUBLIC_KEY');
   ```
3. Replace with your actual public key:
   ```javascript
   emailjs.init('AbCdEfGhIjKlMnOp'); // Your actual key
   ```

4. Find this line (around line 141):
   ```javascript
   emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this)
   ```
5. Replace with your actual IDs:
   ```javascript
   emailjs.sendForm('service_abc123', 'template_xyz789', this)
   ```

### Step 6: Push Changes to GitHub
```powershell
cd c:\Users\piyus\.gemini\antigravity\scratch\django_crud\portfolio_site

git add script.js
git commit -m "Configure EmailJS"
git push
```

Vercel will automatically redeploy your site with the new changes!

---

## Part 4: Test Everything

### Test Your Website
1. Visit: `https://virenvaviya.vercel.app`
2. Check all sections load correctly:
   - ✅ Hero section with "AI/ML Engineer"
   - ✅ About section with skills
   - ✅ Projects section with GitHub projects
   - ✅ Contact section with your details

### Test Contact Form
1. Scroll to the Contact section
2. Fill in:
   - **Name**: Test User
   - **Email**: test@example.com
   - **Message**: This is a test message
3. Click **"Send Message"**
4. You should see: **"✓ Message Sent!"**
5. Check your email (`vrenvaviya2022@gmail.com`) for the message

---

## Troubleshooting

### Contact Form Not Working?
- Check browser console (F12 → Console tab)
- Verify EmailJS credentials are correct
- Make sure you pushed the updated `script.js` to GitHub

### Website Not Updating?
- Vercel auto-deploys when you push to GitHub
- Check **"Deployments"** tab in Vercel dashboard
- Wait 1-2 minutes for deployment to complete

### Domain Already Taken?
- Try variations:
  - `viren-vaviya.vercel.app`
  - `virenvaviya-portfolio.vercel.app`
  - `vaviyaviren.vercel.app`

---

## Next Steps

### 1. Add to Your Resume
```
Portfolio: https://virenvaviya.vercel.app
```

### 2. Add to LinkedIn
- Go to your LinkedIn profile
- Click **"Add profile section"** → **"Featured"**
- Select **"Add link"**
- Paste: `https://virenvaviya.vercel.app`
- Add title: "My Portfolio Website"

### 3. Share on Social Media
Tweet it, share it, show it off! 🚀

### 4. Update Regularly
Whenever you update your code:
```powershell
git add .
git commit -m "Updated portfolio"
git push
```
Vercel will automatically redeploy!

---

## Summary

✅ **Your Portfolio URL**: `https://virenvaviya.vercel.app`  
✅ **Hosting**: Free forever on Vercel  
✅ **SSL**: Automatic HTTPS encryption  
✅ **Deploy Time**: Instant (auto-deploys on git push)  
✅ **Contact Form**: Working with EmailJS  

**Congratulations! Your portfolio is now live! 🎉**

---

## Support

Need help? Contact me or check:
- Vercel Docs: https://vercel.com/docs
- EmailJS Docs: https://www.emailjs.com/docs/
- GitHub Docs: https://docs.github.com/
