# AI/ML Engineer Portfolio

A modern, dark-themed portfolio website showcasing AI/ML projects and expertise.

## Features

- 🎨 Modern dark theme with glassmorphism effects
- 📱 Fully responsive design
- ✉️ Contact form with EmailJS integration
- 🚀 Smooth animations and transitions
- 💼 GitHub projects showcase
- 📊 Skills visualization

## Setup Instructions

### 1. EmailJS Configuration

To enable the contact form:

1. Sign up at [EmailJS](https://www.emailjs.com/)
2. Create an email service (Gmail recommended)
3. Create an email template with these variables:
   - `{{user_name}}` - Visitor's name
   - `{{user_email}}` - Visitor's email
   - `{{message}}` - Message content
4. Get your credentials:
   - Public Key
   - Service ID
   - Template ID
5. Open `script.js` and replace:
   - `'YOUR_PUBLIC_KEY'` with your actual public key
   - `'YOUR_SERVICE_ID'` with your service ID
   - `'YOUR_TEMPLATE_ID'` with your template ID

### 2. Local Testing

Simply open `index.html` in your browser to test locally.

### 3. Deployment

See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed deployment instructions.

**Quick Deploy Options:**
- **Netlify**: Easiest - Connect GitHub repo and auto-deploy
- **Vercel**: Similar to Netlify
- **GitHub Pages**: Free hosting on GitHub

## File Structure

```
portfolio_site/
├── index.html          # Main HTML file
├── style.css           # Styling
├── script.js           # JavaScript functionality
├── README.md           # This file
└── DEPLOYMENT.md       # Deployment guide
```

## Customization

- **Personal Info**: Update contact details in `index.html`
- **Projects**: Modify project cards in the Projects section
- **Skills**: Edit skills in the About section
- **Colors**: Adjust CSS variables in `style.css`

## Technologies Used

- HTML5
- CSS3 (with CSS Variables)
- Vanilla JavaScript
- EmailJS (for contact form)
- Font Awesome (icons)
- Google Fonts (Outfit, Plus Jakarta Sans)

## License

Free to use for personal portfolios.

---

Made with ❤️ by Viren Vaviya
