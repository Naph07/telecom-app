# Telecom Toolbox - Your Skill Up Hub

A comprehensive learning platform designed to empower telecom professionals with hands-on skills and career advancement opportunities. Built with Next.js 15, TypeScript, and Tailwind CSS.

![Telecom Toolbox Dashboard](https://via.placeholder.com/800x400/3B82F6/FFFFFF?text=Telecom+Toolbox+Dashboard)

## 🚀 Features

### 📚 Learning & Development
- **Interactive Labs**: Hands-on virtual environments for practicing telecom skills
- **Learning Paths**: Structured courses covering 5G, Fiber Optics, IoT, and Cloud Telecom
- **Certifications**: Industry-recognized certification programs with progress tracking
- **Skills Assessment**: Radar chart visualization of your technical competencies

### 🌐 Technology Areas
- **5G Technologies**: Network planning, implementation, and optimization
- **Fiber Optics**: Installation, testing, and troubleshooting
- **IoT Integration**: Device management and network integration
- **Cloud Telecom**: Virtual PBX, NFV, and cloud-based solutions

### 👥 Community Features
- **Discussion Forums**: Connect with other telecom professionals
- **Mentorship Program**: Learn from industry experts
- **Collaboration Projects**: Work on open-source telecom projects
- **Knowledge Sharing**: Share resources and best practices

### 📊 Progress Tracking
- **Personal Dashboard**: Overview of your learning progress
- **Skill Visualization**: Interactive radar charts showing competency levels
- **Achievement System**: Track completed courses, lab hours, and certifications
- **Community Engagement**: Monitor your participation and contributions

## 🛠️ Technologies Used

- **Framework**: Next.js 15 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui
- **Icons**: Lucide React
- **Charts**: Recharts
- **Theme**: next-themes for dark/light mode

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js 18.18 or later
- npm, yarn, pnpm, or bun package manager
- Git (for cloning the repository)

## 🚀 Installation

### Option 1: Quick Start (Recommended)

1. **Clone the repository**
   \`\`\`bash
   git clone https://github.com/yourusername/telecom-toolbox.git
   cd telecom-toolbox
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   \`\`\`

3. **Run the development server**
   \`\`\`bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   \`\`\`

4. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

### Option 2: Static Export (For Hosting Issues)

If you encounter issues with the development server:

1. **Build the static site**
   \`\`\`bash
   npm run build
   \`\`\`

2. **Serve the static files**
   \`\`\`bash
   # Install serve globally
   npm install -g serve
   
   # Serve the built files
   serve -s out
   \`\`\`

## 📁 Project Structure

\`\`\`
telecom-toolbox/
├── app/                          # Next.js App Router pages
│   ├── certifications/           # Certification tracking page
│   ├── community/               # Community forums and discussions
│   ├── labs/                    # Interactive labs page
│   ├── learning/                # Learning paths page
│   ├── technologies/            # Technology-specific pages
│   │   └── 5g/                  # 5G technology deep dive
│   ├── globals.css              # Global styles and CSS variables
│   ├── layout.tsx               # Root layout component
│   └── page.tsx                 # Dashboard homepage
├── components/                   # Reusable React components
│   ├── dashboard/               # Dashboard-specific components
│   │   ├── dashboard-header.tsx
│   │   ├── dashboard-shell.tsx
│   │   ├── overview-stats.tsx
│   │   ├── recommended-courses.tsx
│   │   ├── skills-progress.tsx
│   │   ├── recent-activity.tsx
│   │   └── upcoming-certifications.tsx
│   ├── ui/                      # shadcn/ui components
│   ├── main-nav.tsx             # Main navigation component
│   ├── sidebar.tsx              # Sidebar navigation
│   ├── user-nav.tsx             # User dropdown menu
│   ├── mode-toggle.tsx          # Dark/light mode toggle
│   └── theme-provider.tsx       # Theme context provider
├── public/                      # Static assets
├── tailwind.config.ts           # Tailwind CSS configuration
├── next.config.js               # Next.js configuration
├── package.json                 # Dependencies and scripts
└── README.md                    # Project documentation
\`\`\`

## 🎨 Customization

### Color Scheme
The project uses a custom color palette defined in `app/globals.css`:
- **Primary**: Blue (#3B82F6) - Used for main actions and highlights
- **Secondary**: Cyan (#06B6D4) - Used for secondary elements
- **Accent**: Purple (#8B5CF6) - Used for special highlights

### Adding New Technology Areas
1. Create a new page in `app/technologies/[technology-name]/page.tsx`
2. Add the navigation link in `components/sidebar.tsx`
3. Create corresponding components in `components/dashboard/`

### Customizing the Dashboard
- Modify `components/dashboard/overview-stats.tsx` to change statistics
- Update `components/dashboard/skills-progress.tsx` to adjust skill categories
- Edit `components/dashboard/recommended-courses.tsx` to change course recommendations

## 🔧 Troubleshooting

### Common Issues

#### Slow Development Server
If you see "Slow filesystem detected" message:

1. **Exclude from antivirus**: Add your project folder to antivirus exclusions
2. **Use different port**: Run `npm run dev -- -p 3001`
3. **Clear cache**: Run `npm cache clean --force`

#### Port Already in Use
\`\`\`bash
# Check what's using port 3000
netstat -ano | findstr :3000

# Use a different port
npm run dev -- -p 3001
\`\`\`

#### Build Errors
\`\`\`bash
# Clear Next.js cache
rm -rf .next

# Reinstall dependencies
rm -rf node_modules package-lock.json
npm install
\`\`\`

### Performance Optimization

1. **Enable static export** for better performance:
   \`\`\`javascript
   // next.config.js
   module.exports = {
     output: 'export',
     images: { unoptimized: true }
   }
   \`\`\`

2. **Use environment variables** for configuration:
   \`\`\`bash
   # .env.local
   NEXT_PUBLIC_APP_NAME="Telecom Toolbox"
   NEXT_PUBLIC_API_URL="https://api.example.com"
   \`\`\`

## 🚀 Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Deploy automatically on every push

### Static Hosting
1. Build the static site: `npm run build`
2. Upload the `out` folder to any static hosting service

### Docker
\`\`\`dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
\`\`\`

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Development Guidelines
- Use TypeScript for all new components
- Follow the existing code style and structure
- Add proper TypeScript types for all props and functions
- Test your changes thoroughly before submitting

## 📝 Scripts

\`\`\`bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript type checking
\`\`\`

## 🔒 Environment Variables

Create a `.env.local` file in the root directory:

\`\`\`bash
# App Configuration
NEXT_PUBLIC_APP_NAME="Telecom Toolbox"
NEXT_PUBLIC_APP_VERSION="1.0.0"

# API Configuration (if needed)
NEXT_PUBLIC_API_URL="https://api.example.com"
API_SECRET_KEY="your-secret-key"

# Database (if implementing backend)
DATABASE_URL="your-database-url"
\`\`\`

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - The React framework for production
- [Tailwind CSS](https://tailwindcss.com/) - A utility-first CSS framework
- [shadcn/ui](https://ui.shadcn.com/) - Beautifully designed components
- [Lucide](https://lucide.dev/) - Beautiful & consistent icon toolkit
- [Recharts](https://recharts.org/) - Redefined chart library built with React

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Troubleshooting](#-troubleshooting) section
2. Search existing [GitHub Issues](https://github.com/yourusername/telecom-toolbox/issues)
3. Create a new issue with detailed information about your problem

## 🗺️ Roadmap

- [ ] User authentication and profiles
- [ ] Real-time collaboration features
- [ ] Mobile app development
- [ ] Integration with telecom APIs
- [ ] Advanced analytics dashboard
- [ ] Multi-language support
- [ ] Offline mode capabilities

---

**Built with ❤️ for the telecom community**
This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
