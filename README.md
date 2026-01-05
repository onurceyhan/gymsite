# XEON Gym - Transform Your Body

A modern, cyberpunk-themed gym website built with Vue 3 and Vite. Features a stunning neon green and dark purple color scheme with smooth animations and a futuristic design aesthetic.

![XEON Gym](https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=1200&q=80)

## ✨ Features

- 🎨 **Modern Cyberpunk Design** - Eye-catching neon green and dark purple color scheme
- 💪 **Responsive Layout** - Perfect display on all devices
- ⚡ **Fast Performance** - Built with Vue 3 and Vite for lightning-fast loading
- 🎭 **Smooth Animations** - Glitch effects and smooth transitions
- 📱 **Mobile Friendly** - Fully responsive hamburger menu and adaptive layouts
- 🎯 **Multiple Sections**:
  - Hero section with call-to-action
  - Classes showcase with 6 different programs
  - Professional trainers gallery
  - Pricing plans (Basic, Premium, Elite)
  - Contact form with info cards
  - Social media integration

## 🚀 Quick Start

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/onurceyhan/gymsite.git
cd gymsite
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and visit `http://localhost:5173`

## 🛠️ Build for Production

Create an optimized production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## 🌐 Deploy to Vercel

### Method 1: Deploy via Vercel CLI

1. Install Vercel CLI globally:
```bash
npm install -g vercel
```

2. Deploy to Vercel:
```bash
vercel
```

3. Follow the prompts and your site will be live!

### Method 2: Deploy via Vercel Dashboard

1. Push your code to GitHub:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/gymsite.git
git push -u origin main
```

2. Go to [Vercel](https://vercel.com) and sign in

3. Click "Add New Project"

4. Import your GitHub repository

5. Configure the project:
   - **Framework Preset**: Vite
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`

6. Click "Deploy" and wait for the deployment to complete

7. Your site will be live at `https://your-project-name.vercel.app`

### Environment Variables (if needed)

If you need to add environment variables:

1. Go to your project settings on Vercel
2. Navigate to "Environment Variables"
3. Add your variables (e.g., `VITE_API_URL`)
4. Redeploy your project

## 📁 Project Structure

```
gymsite/
├── public/              # Static assets
├── src/
│   ├── components/      # Vue components
│   │   ├── NavBar.vue
│   │   ├── Hero.vue
│   │   ├── Classes.vue
│   │   ├── Trainers.vue
│   │   ├── Pricing.vue
│   │   ├── Contact.vue
│   │   └── Footer.vue
│   ├── App.vue         # Root component
│   ├── main.js         # Application entry point
│   └── style.css       # Global styles
├── index.html          # HTML template
├── package.json        # Dependencies and scripts
├── vite.config.js      # Vite configuration
└── README.md          # Project documentation
```

## 🎨 Customization

### Colors

The color scheme can be customized in `src/style.css`:

```css
:root {
  --neon-green: #c8ff00;
  --neon-glow: #a8df00;
  --dark-purple: #1a0f2e;
  --mid-purple: #2d1b4e;
  --light-purple: #4a2f6e;
  --text-light: #e8e8e8;
  --text-dark: #1a1a1a;
}
```

### Images

Replace the Unsplash image URLs in the components with your own images to customize the look.

### Content

Edit the content directly in each Vue component file:
- Hero text: `src/components/Hero.vue`
- Classes: `src/components/Classes.vue`
- Trainers: `src/components/Trainers.vue`
- Pricing: `src/components/Pricing.vue`
- Contact info: `src/components/Contact.vue`

## 📦 Tech Stack

- **Vue 3** - Progressive JavaScript framework
- **Vite** - Next generation frontend tooling
- **Vue Router** - Official router for Vue.js
- **CSS3** - Modern styling with custom properties
- **Google Fonts** - Exo 2 & Bebas Neue font families

## 🔗 Links

- **GitHub**: [github.com/onurceyhan](https://github.com/onurceyhan)
- **LinkedIn**: [linkedin.com/in/onur.ceyhan](https://linkedin.com/in/onur.ceyhan)
- **Live Demo**: Deploy to Vercel to get your live demo URL

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Developer

**Onur Ceyhan**

- GitHub: [@onurceyhan](https://github.com/onurceyhan)
- LinkedIn: [onur.ceyhan](https://linkedin.com/in/onur.ceyhan)

## 🙏 Acknowledgments

- Design inspiration from cyberpunk and modern fitness aesthetics
- Stock images from [Unsplash](https://unsplash.com)
- Icons and emojis for visual enhancement

---

⭐ **Star this repo** if you found it helpful!

Built with ❤️ and 💪 by Onur Ceyhan

