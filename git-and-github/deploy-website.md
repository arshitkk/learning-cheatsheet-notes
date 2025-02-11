# How to Deploy Website on GitHub Pages

## **INDEX:**

1. [**Deploying a Normal Website (Static Files)**](#1-deploying-a-normal-website-static-files)

2. [**Deploying a React App**](#2-deploying-a-react-app)

---

## **1. Deploying a Normal Website (Static Files)**

### Steps:

1. **Link Your GitHub Repo**

   - Push the code to your github and make a working repo like normally

2. **Go to GitHub Repository Settings**

   - Navigate to the `Settings` tab of your repository.

3. **Set Up GitHub Pages**

   - In the **Pages** section under `Code and automation`, select the branch (`main`) to deploy from.
   - Choose `/root` as the folder (for static files).
   - Save your settings.

4. **Deploy**
   - After setting up, GitHub Pages will automatically deploy your site
     (_might take some time_) and will give u link like -> `https://<your-username>.github.io/<repo-name>/`.

[Go to top ↑](#index)

---

## **2. Deploying a React App**

### Steps:

1. **Prepare Your React App for Deployment**

   - First, make sure your React app is ready by building it:

   ```bash
   npm run build
   ```

2. **Install `gh-pages`**

   - Install the `gh-pages` package in your React app:

   ```bash
   npm install gh-pages --save-dev
   ```

3. **Update `package.json`**

   - Add the following to your `package.json`:

   **Add `homepage` key**:

   ```json
   "homepage": "https://<your-username>.github.io/<repo-name>/"
   ```

   **Add `predeploy` and `deploy` scripts**:

   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d build"
   }
   ```

4. **Push Changes to GitHub**

   - After making the necessary changes to `package.json`, commit and push them to GitHub:

   ```bash
   git add .
   git commit -m "Added deployment configuration"
   git push -u origin main
   ```

5. **Run the Deploy Script**

   - Run the deployment command:

   ```bash
   npm run deploy
   ```

6. **Go to GitHub Pages Settings**

   - Go to the **Settings** tab of your repository.
   - In the **Pages** section, under **Source**, if not selected then choose `gh-pages` branch and save.

7. **Access Your React App**
   - Your React app will be live at `https://<your-username>.github.io/<repo-name>/`.

[Go to top ↑](#index)

---
