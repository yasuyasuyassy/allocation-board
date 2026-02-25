## Host Allocation Board on GitHub Pages (free)

This project (`AllocationWebGitHub`) is a **Blazor WebAssembly** app, which can be hosted as static files on GitHub Pages.

### 1. Create a GitHub repo

1. On GitHub, create a new repository, e.g. `allocation-board`.
2. In PowerShell:

   ```powershell
   cd "C:\Users\socce\OneDrive\デスクトップ\App\AllocationWebGitHub"
   git init
   git add .
   git commit -m "Initial commit - Allocation board web"
   git branch -M main
   git remote add origin https://github.com/<your-user>/allocation-board.git
   git push -u origin main
   ```

### 2. Enable GitHub Pages

1. In the repo on GitHub, go to **Settings → Pages**.
2. Under **Build and deployment**, choose:
   - **Source**: GitHub Actions
3. Save.

The workflow file `.github/workflows/deploy-gh-pages.yml` will:
- Build the app on every push to `main`,
- Publish it to GitHub Pages.

### 3. Find your public URL

After the workflow runs successfully (check the **Actions** tab), your app will be available at:

- `https://<your-user>.github.io/allocation-board/`

Share that URL with your friend.

