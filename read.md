# Professional Portfolio Website

A modern, responsive portfolio website with contact form functionality and email notifications. Built with HTML, CSS, JavaScript (frontend) and Node.js, Express (backend).

## Features

- ✨ Modern, responsive design with smooth animations
- 📱 Mobile-friendly interface
- 📧 Contact form with email notifications
- 🚀 Fast loading and optimized performance
- 🔒 Security features (rate limiting, input validation)
- 📊 Professional sections: About, Skills, Projects, Contact

## Tech Stack

**Frontend:**
- HTML5, CSS3, JavaScript
- Font Awesome icons
- Responsive design

**Backend:**
- Node.js
- Express.js
- Nodemailer (email functionality)
- Security middleware (Helmet, CORS, Rate Limiting)

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/professional-portfolio.git
cd professional-portfolio
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Setup

Create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Edit the `.env` file with your email credentials:

```env
PORT=3000
NODE_ENV=production
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
NOTIFICATION_EMAIL=your-email@gmail.com
```

### 4. Gmail App Password Setup (Recommended)

1. Enable 2-Step Verification on your Gmail account
2. Go to Google Account settings → Security
3. Under "2-Step Verification," click "App passwords"
4. Generate an app password for "Mail"
5. Use this app password in your `.env` file (not your regular Gmail password)

### 5. Customize Content

Edit the `public/index.html` file to personalize:

- Replace "Your Name" with your actual name
- Update the profile image URL
- Modify the about section
- Add your actual projects
- Update social media links
- Change skills and technologies

### 6. Create Public Directory

```bash
mkdir public
# Move your index.html file to the public directory
mv index.html public/
```

### 7. Run the Application

For development:
```bash
npm run dev
```

For production:
```bash
npm start
```

Visit `http://localhost:3000` to view your portfolio.

## Project Structure

```
professional-portfolio/
├── public/
│   └── index.html          # Frontend HTML file
├── server.js               # Backend server
├── package.json           # Dependencies and scripts
├── .env                   # Environment variables (create this)
├── .env.example          # Environment template
├── .gitignore           # Git ignore file
└── README.md           # This file
```

## Deployment Options

### Heroku Deployment

1. Install Heroku CLI
2. Create a Heroku app:
   ```bash
   heroku create your-portfolio-name
   ```

3. Set environment variables on Heroku:
   ```bash
   heroku config:set EMAIL_USER=your-email@gmail.com
   heroku config:set EMAIL_PASS=your-app-password
   heroku config:set NOTIFICATION_EMAIL=your-email@gmail.com
   ```

4. Deploy:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push heroku main
   ```

### Vercel Deployment

1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in your project directory
3. Set environment variables in Vercel dashboard
4. Deploy with `vercel --prod`

### Netlify Deployment

1. Build the project: `npm run build`
2. Deploy the `public` folder to Netlify
3. Set environment variables in Netlify dashboard
4. Configure serverless functions for the backend

## Email Service Configuration

### Gmail (Recommended)
- Use app passwords for better security
- Supports up to 500 emails per day for free accounts

### Other Email Services
Uncomment and configure the SMTP settings in `.env`:

```env
SMTP_HOST=smtp.your-provider.com
SMTP_PORT=587
SMTP_SECURE=false
SMTP_USER=your-email@domain.com
SMTP_PASS=your-password
```

Popular SMTP services:
- **SendGrid**: Professional email service
- **Mailgun**: Developer-focused email API
- **Outlook**: Microsoft email service
- **Yahoo Mail**: Alternative free service

## Customization Guide

### Colors and Styling
Edit the CSS in `public/index.html` to match your brand:

```css
:root {
  --primary-color: #667eea;
  --secondary-color: #764ba2;
  --text-color: #333;
  --background-color: #fff;
}
```

### Adding New Sections
1. Add HTML structure
2. Add corresponding CSS styles
3. Update navigation links
4. Add smooth scrolling JavaScript

### Contact Form Fields
To add new fields:
1. Add HTML input in the contact form
2. Update validation in `server.js`
3. Include new fields in email templates

## Security Features

- **Rate Limiting**: 5 contact form submissions per 15 minutes per IP
- **Input Validation**: Server-side validation for all form fields
- **Sanitization**: HTML and script tag removal from inputs
- **Helmet.js**: Security headers
- **CORS**: Cross-origin resource sharing protection

## Troubleshooting

### Email Not Sending
1. Check your email credentials in `.env`
2. Verify Gmail app password is correct
3. Check console for error messages
4. Test email configuration with a simple test

### Port Already in Use
```bash
# Kill process on port 3000
lsof -ti:3000 | xargs kill -9
```

### Environment Variables Not Loading
1. Ensure `.env` file is in root directory
2. Restart the server after changing `.env`
3. Check for typos in variable names

## Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you have any questions or run into issues:

1. Check the troubleshooting section above
2. Review the GitHub issues page
3. Create a new issue with detailed information

## Acknowledgments

- Font Awesome for icons
- Google Fonts for typography
- Inspiration from modern portfolio designs

---

⭐ If you found this helpful, please give it a star on GitHub!