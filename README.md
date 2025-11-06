# Vue Jobs - Job Listing Application

A modern, full-featured job listing application built with Vue 3, Vite, and Tailwind CSS. This application provides a complete CRUD (Create, Read, Update, Delete) interface for managing job postings with a beautiful, responsive UI.

![Vue.js](https://img.shields.io/badge/Vue.js-3.5-4FC08D?style=flat&logo=vue.js&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7.1-646CFF?style=flat&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🚀 Features

- **Modern UI/UX**: Clean and responsive interface built with Tailwind CSS
- **Full CRUD Operations**: Create, read, update, and delete job listings
- **Dynamic Routing**: Client-side routing with Vue Router
- **Toast Notifications**: User-friendly feedback with Vue Toastification
- **JSON Server Backend**: Mock REST API for development
- **Component-Based Architecture**: Reusable Vue 3 components
- **Loading States**: Elegant loading indicators with Vue Spinner
- **404 Handling**: Custom not-found page for invalid routes
- **Icon Integration**: Beautiful icons with PrimeIcons

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js**: `^20.19.0` or `>=22.12.0`
- **npm**: Comes with Node.js

## 🛠️ Installation

1. **Clone the repository**

```bash
git clone <repository-url>
cd vue-sampling
```

2. **Install dependencies**

```bash
npm install
```

## 🚦 Running the Application

To run the application, you need to start both the Vite development server and the JSON server.

### Option 1: Using Two Terminal Windows

**Terminal 1 - Start the Development Server:**

```bash
npm run dev
```

**Terminal 2 - Start the JSON Server:**

```bash
npm run server
```

### Option 2: Using a Process Manager (Recommended)

You can use a tool like `concurrently` to run both servers simultaneously. First, install it:

```bash
npm install --save-dev concurrently
```

Then add this script to your `package.json`:

```json
"scripts": {
  "start": "concurrently \"npm run dev\" \"npm run server\""
}
```

Now you can run both servers with:

```bash
npm start
```

### Accessing the Application

- **Frontend**: Open your browser and navigate to `http://localhost:5173` (or the port shown in your terminal)
- **API Server**: JSON Server runs on `http://localhost:5000`

## 📁 Project Structure

```
vue-sampling/
├── public/              # Static assets
│   └── favicon.ico
├── src/
│   ├── assets/          # Images, styles, and other assets
│   │   ├── img/
│   │   └── main.css
│   ├── components/      # Reusable Vue components
│   │   ├── BackButton.vue
│   │   ├── Card.vue
│   │   ├── Hero.vue
│   │   ├── HomeCards.vue
│   │   ├── JobListing.vue
│   │   ├── JobListings.vue
│   │   └── Navbar.vue
│   ├── views/           # Page components
│   │   ├── Home.vue
│   │   ├── Jobs.vue
│   │   ├── Job.vue
│   │   ├── AddJob.vue
│   │   ├── EditJob.vue
│   │   └── NotFound.vue
│   ├── router/          # Vue Router configuration
│   │   └── index.js
│   ├── App.vue          # Root component
│   ├── main.js          # Application entry point
│   └── jobs2.json       # Mock database for JSON Server
├── package.json
├── vite.config.js       # Vite configuration
├── tailwind.config.js   # Tailwind CSS configuration
└── README.md
```

## 🧩 Key Components

### Views

- **Home**: Landing page with hero section and featured job listings
- **Jobs**: Complete list of all job postings
- **Job**: Detailed view of a single job posting
- **AddJob**: Form to create a new job listing
- **EditJob**: Form to update an existing job listing
- **NotFound**: 404 error page for invalid routes

### Components

- **Navbar**: Navigation bar with routing links
- **Hero**: Hero section for the landing page
- **HomeCards**: Card components for the home page
- **JobListings**: Container for displaying multiple job listings
- **JobListing**: Individual job listing card
- **Card**: Reusable card wrapper component
- **BackButton**: Navigation button to go back

## 📦 Tech Stack

### Core

- **[Vue 3](https://vuejs.org/)** (v3.5.22) - Progressive JavaScript framework
- **[Vite](https://vitejs.dev/)** (v7.1.11) - Next-generation frontend tooling
- **[Vue Router](https://router.vuejs.org/)** (v4.6.3) - Official router for Vue.js

### Styling

- **[Tailwind CSS](https://tailwindcss.com/)** (v3.4.18) - Utility-first CSS framework
- **[PostCSS](https://postcss.org/)** (v8.5.6) - CSS transformation tool
- **[Autoprefixer](https://github.com/postcss/autoprefixer)** (v10.4.21) - CSS vendor prefixing

### Libraries

- **[Axios](https://axios-http.com/)** (v1.13.2) - HTTP client for API requests
- **[JSON Server](https://github.com/typicode/json-server)** (v1.0.0-beta.3) - Mock REST API
- **[Vue Toastification](https://vue-toastification.maronato.dev/)** (v2.0.0-rc.5) - Toast notification library
- **[Vue Spinner](https://www.npmjs.com/package/vue-spinner)** (v1.0.4) - Loading spinners
- **[PrimeIcons](https://primevue.org/icons/)** (v7.0.0) - Icon library

### Development

- **[@vitejs/plugin-vue](https://github.com/vitejs/vite-plugin-vue)** (v6.0.1) - Official Vue plugin for Vite
- **[vite-plugin-vue-devtools](https://github.com/vuejs/devtools-next)** (v8.0.3) - Vue DevTools integration

## 🔧 Available Scripts

| Script            | Description                                   |
| ----------------- | --------------------------------------------- |
| `npm run dev`     | Start Vite development server with hot-reload |
| `npm run build`   | Build the application for production          |
| `npm run preview` | Preview the production build locally          |
| `npm run server`  | Start JSON Server on port 5000                |

## 🌐 API Endpoints

The JSON Server provides the following endpoints:

- `GET /jobs` - Get all jobs
- `GET /jobs/:id` - Get a specific job
- `POST /jobs` - Create a new job
- `PUT /jobs/:id` - Update an existing job
- `DELETE /jobs/:id` - Delete a job

## 🎨 Customization

### Tailwind CSS

Modify `tailwind.config.js` to customize your design system:

```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        // Add your custom colors
      },
    },
  },
};
```

### Vite Configuration

Update `vite.config.js` to adjust build settings and plugins.

## 💡 Development Tips

### Recommended IDE Setup

- **[VS Code](https://code.visualstudio.com/)** + **[Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar)**
- Disable Vetur if you have it installed (it conflicts with Vue Official extension)

### Browser DevTools

**Chromium-based browsers (Chrome, Edge, Brave, etc.):**

- [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
- [Turn on Custom Object Formatter in Chrome DevTools](http://bit.ly/object-formatters)

**Firefox:**

- [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
- [Turn on Custom Object Formatter in Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## 🏗️ Building for Production

1. **Build the application:**

```bash
npm run build
```

2. **Preview the production build:**

```bash
npm run preview
```

The build output will be in the `dist/` directory, ready to be deployed to any static hosting service.

## 🚀 Deployment

This application can be deployed to various platforms:

- **[Vercel](https://vercel.com/)**: Zero-configuration deployment
- **[Netlify](https://www.netlify.com/)**: Continuous deployment from Git
- **[GitHub Pages](https://pages.github.com/)**: Free hosting for static sites
- **[Firebase Hosting](https://firebase.google.com/docs/hosting)**: Fast and secure web hosting

### Note on JSON Server

JSON Server is for development only. For production, you'll need to:

- Replace JSON Server with a real backend API (Node.js, Django, Laravel, etc.)
- Update the Axios base URL in your components to point to your production API

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact

For questions or support, please open an issue in the repository.

## 🙏 Acknowledgments

- Vue.js team for the amazing framework
- Tailwind CSS for the utility-first CSS framework
- All the open-source contributors whose libraries made this project possible

---

**Built with ❤️ using Vue 3 and Vite**
