# CCHendrix Website Deployment Guide

## Deployment Instructions

This is a static website that can be deployed to any web hosting service. Here are some popular options:

### Option 1: GitHub Pages (Free)
1. Go to your repository settings
2. Navigate to "Pages" section
3. Select the branch (main or current branch)
4. Select root folder as the source
5. Your site will be available at: `https://d86petersen.github.io/CCHendrix/`

### Option 2: Netlify (Free)
1. Sign up at [netlify.com](https://netlify.com)
2. Click "New site from Git"
3. Connect your GitHub repository
4. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: `/`
5. Click "Deploy site"
6. You can connect your custom domain in the site settings

### Option 3: Vercel (Free)
1. Sign up at [vercel.com](https://vercel.com)
2. Click "New Project"
3. Import your GitHub repository
4. Deploy settings will be auto-detected
5. Click "Deploy"
6. Connect your custom domain in project settings

### Option 4: Traditional Web Hosting
1. Upload all files via FTP/SFTP to your web host:
   - index.html
   - styles.css
   - script.js
   - README.md (optional)
2. Make sure index.html is in the root directory
3. Your domain should now display the website

## Files Structure
```
/
├── index.html      # Main HTML file
├── styles.css      # All CSS styles
├── script.js       # JavaScript functionality
└── README.md       # Project documentation
```

## Custom Domain Setup
Once deployed, you can connect your custom domain by:
1. Adding a CNAME record pointing to your hosting provider
2. Following your hosting provider's custom domain instructions
3. Enabling SSL/HTTPS for security

## Customization
To customize the website:
- **Logo**: Replace the text logo in `index.html` with an `<img>` tag pointing to your logo file
- **Colors**: Modify the CSS variables in `styles.css` under `:root`
- **Content**: Edit text directly in `index.html`
- **Contact Info**: Update email, phone, and address in both the contact section and footer
- **Images**: Add your own images by placing them in an `images/` folder and updating the src attributes

## Contact Form Integration
The contact form currently logs submissions to the browser console. To make it functional:
1. Use a service like Formspree, Netlify Forms, or Web3Forms
2. Or integrate with your backend API
3. Update the form submission handler in `script.js`

## Browser Support
The website is compatible with:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance
The website is optimized for performance:
- No heavy frameworks (vanilla JavaScript)
- Minimal external dependencies (only Google Fonts)
- Responsive images and optimized CSS
- Fast loading times

## Need Help?
If you need assistance with deployment or customization, please refer to your hosting provider's documentation or contact support.
