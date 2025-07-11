# Suhana Gomber - Portfolio Website

A beautiful, responsive portfolio website built with React, TypeScript, and Tailwind CSS. Features a modern pink-themed design with smooth animations, typing effects, and a professional layout showcasing experience in talent acquisition and business development.

## 🌟 Features

- **Modern Design**: Clean, minimalist design with a soft pink color scheme
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Loading Animation**: Custom typing animation with "HI, I AM SUHANA"
- **Smooth Scrolling**: Apple-inspired smooth scroll behavior
- **Interactive Elements**: Hover effects, animations, and micro-interactions
- **Contact Form**: Functional contact form with email integration
- **Professional Sections**: About, Experience, Education, Coursework, Gallery, and Contact

## 🚀 Quick Start

### Prerequisites

Make sure you have the following installed on your system:
- **Node.js** (version 16.0 or higher)
- **npm** (comes with Node.js)

### Installation

1. **Clone or download the project**
   ```bash
   # If you have the project files, navigate to the project directory
   cd suhana-portfolio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   - The application will automatically open at `http://localhost:5173`
   - If it doesn't open automatically, manually navigate to the URL

## 📁 Project Structure

```
suhana-portfolio/
├── public/
│   └── vite.svg
├── src/
│   ├── components/
│   │   ├── About.tsx
│   │   ├── Contact.tsx
│   │   ├── Coursework.tsx
│   │   ├── Education.tsx
│   │   ├── Experience.tsx
│   │   ├── Extracurricular.tsx
│   │   ├── Gallery.tsx
│   │   ├── Header.tsx
│   │   ├── Hero.tsx
│   │   └── LoadingScreen.tsx
│   ├── App.css
│   ├── App.tsx
│   ├── index.css
│   ├── main.tsx
│   └── vite-env.d.ts
├── index.html
├── package.json
├── tailwind.config.js
├── tsconfig.json
├── vite.config.ts
└── README.md
```

## 🛠️ Available Scripts

- **`npm run dev`** - Starts the development server
- **`npm run build`** - Builds the app for production
- **`npm run preview`** - Preview the production build locally
- **`npm run lint`** - Run ESLint to check for code issues

## 🎨 Customization

### Colors
The website uses a soft pink color scheme. Main colors are defined in:
- `src/App.css` - Custom CSS variables and animations
- `tailwind.config.js` - Tailwind CSS configuration

### Content
To update personal information:
- **Contact Info**: Update in `src/components/Contact.tsx`
- **Professional Experience**: Modify `src/components/Experience.tsx`
- **Education**: Update `src/components/Education.tsx`
- **About Section**: Edit `src/components/About.tsx`

### Images
- Profile images are sourced from Pexels
- To use custom images, replace the URLs in respective components
- Gallery images can be updated in `src/components/Gallery.tsx`

## 📧 Contact Form

The contact form uses EmailJS to send emails directly without opening the user's email client.

### EmailJS Setup (Required for Contact Form)

1. **Create EmailJS Account**
   - Go to [EmailJS.com](https://www.emailjs.com/)
   - Sign up for a free account

2. **Create Email Service**
   - Add a new email service (Gmail, Outlook, etc.)
   - Connect your email account
   - Note the Service ID

3. **Create Email Template**
   - Create a new email template
   - Use these template variables:
     - `{{from_name}}` - Sender's name
     - `{{from_email}}` - Sender's email
     - `{{subject}}` - Email subject
     - `{{message}}` - Email message
   - Set recipient email to: suhana0627@gmail.com
   - Note the Template ID

4. **Get Public Key**
   - Go to Account settings
   - Copy your Public Key

5. **Update Configuration**
   - Open `src/components/Contact.tsx`
   - Replace the following values:
     ```javascript
     const serviceId = 'your_service_id';
     const templateId = 'your_template_id';
     const publicKey = 'your_public_key';
     ```

### Template Example
```
Subject: New Portfolio Contact: {{subject}}

From: {{from_name}} ({{from_email}})
Subject: {{subject}}

Message:
{{message}}
```

## 🌐 Deployment

### Build for Production
```bash
npm run build
```

The build files will be generated in the `dist/` folder.

### Deploy to Netlify (Recommended)
1. Build the project: `npm run build`
2. Upload the `dist/` folder to Netlify
3. Or connect your Git repository for automatic deployments

### Deploy to Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run: `vercel`
3. Follow the prompts

## 🔧 Technologies Used

- **React 18** - Frontend framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Utility-first CSS framework
- **Vite** - Build tool and development server
- **Lucide React** - Icon library
- **CSS Animations** - Custom animations and transitions

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🐛 Troubleshooting

### Common Issues

1. **Port already in use**
   ```bash
   # Kill the process using port 5173
   npx kill-port 5173
   # Then restart the dev server
   npm run dev
   ```

2. **Dependencies not installing or Rollup native module errors**
   ```bash
   # Clear npm cache and reinstall (fixes Apple Silicon Mac issues)
   npm cache clean --force
   rm -rf node_modules package-lock.json
   npm install
   ```

3. **EmailJS environment variables not working**
   ```bash
   # Make sure environment variables start with VITE_
   # Restart development server after creating/updating .env file
   npm run dev
   ```

4. **Build errors**
   ```bash
   # Check for TypeScript errors
   npm run lint
   # Fix any issues and rebuild
   npm run build
   ```

## 📞 Support

If you encounter any issues or have questions:
- Check the browser console for error messages
- Ensure all dependencies are properly installed
- Verify Node.js version compatibility

## 📄 License

This project is for personal portfolio use.

---

**Built with ❤️ by Suhana Gomber**