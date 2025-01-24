# **Next.js Report Application Documentation**

## **Overview**
This project is a Next.js-based reporting application designed to generate and display reports. The app uses a static export for deployment to GitHub Pages, ensuring it is lightweight and accessible.

Key features:
- Built with Next.js 15 and React 18.
- Styled using TailwindCSS.
- Hosted on GitHub Pages for easy public access.

---

## **Local Setup**

### **Prerequisites**
1. Node.js (version 18 or above) and npm installed.
2. A text editor 

### **Steps to Set Up Locally**
1. Clone the repository:
   ```bash
   git clone https://github.com/username/next-report-app.git
   cd next-report-app
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the development server:
   ```bash
   npm run dev
   ```
4. Open the app in your browser:
   ```
   http://localhost:3000
   ```

---

## **CI/CD Pipeline Configuration**

This project uses GitHub Actions to automate building, testing, and deploying the app.

### **Pipeline Features**
- **Build Check**: Runs `npm run build` to verify the app compiles successfully.
- **Testing**: Executes unit tests with `vitest`.
- **Deployment**: Deploys the static export to GitHub Pages using `gh-pages`.

### **Workflow File**
The GitHub Actions workflow (`.github/workflows/deploy.yml`) includes:
- **Trigger**: Pushes to the `main` branch.
- **Steps**:
  1. **Checkout Code**: Fetches the repository.
  2. **Install Dependencies**: Installs npm packages.
  3. **Build the App**: Runs the Next.js build process.
  4. **Deploy**: Pushes the built files to the `gh-pages` branch.

---

## **Deployment Process**

### **Hosting Platform**
The app is hosted on **GitHub Pages** at:
[https://cadred000.github.io/next-report-app](https://cadred000.github.io/next-report-app)

### **Deployment Steps**
1. Build and export the app:
   ```bash
   npm run build
   ```
2. Deploy to GitHub Pages:
   ```bash
   npm run deploy
   ```
   The `gh-pages` package automates pushing the static files to the `gh-pages` branch.

---

### **Known Limitations** 
1. Github pages cannot handle server side or dynamic routes

2. Sometimes it may be necessary to clear the browser cache and redeploy
