# The Income Equation — Landing Page

Landing page for **The Income Equation** by Vlad Ost. Hosted on GitHub Pages at [theincomeequation.com](https://theincomeequation.com).

## What to do before publishing

1. **Book cover**  
   Export your Canva cover and save it as `images/cover.png` (or `cover.jpg`). The page already references `images/cover.png`; if you use another name, update the `src` in `index.html`.

2. **Book description**  
   Replace the placeholder tagline in `index.html` (inside the `<p class="tagline">` block) with your short, catchy text.

3. **Substack link**  
   In `index.html`, replace `https://YOUR-SUBSTACK-URL.substack.com` with your real Substack URL (e.g. `https://vladost.substack.com`).

4. **Optional: more book photos**  
   To add extra photos of the book, put them in `images/` (e.g. `photo1.jpg`, `photo2.jpg`) and uncomment the gallery block in `index.html`, then fix the `src` paths.

## Publishing on GitHub Pages

1. Create a new repository on GitHub (e.g. `theincomeequation` or `theincomeequation-com`).

2. Push this folder to the repo:
   ```bash
   git init
   git add .
   git commit -m "Initial landing page"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```

3. In the repo: **Settings → Pages**:
   - **Source**: Deploy from a branch
   - **Branch**: `main` (or `master`), folder **/ (root)**
   - Save. The site will be at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

4. **Custom domain (Namecheap)**  
   The file `CNAME` already contains `theincomeequation.com`. After GitHub Pages is working:
   - In the same **Pages** settings, under **Custom domain**, enter `theincomeequation.com` and save.
   - In Namecheap: **Domain List → Manage** for theincomeequation.com → **Advanced DNS**:
     - Add **A Record**: Host `@`, Value `185.199.108.153` (and optionally add `185.199.109.153`, `185.199.110.153`, `185.199.111.153` for redundancy).
     - Add **CNAME Record**: Host `www`, Value `YOUR-USERNAME.github.io` (replace with your GitHub username).
   - Wait for DNS to propagate (up to 24–48 hours). Then in GitHub Pages settings, enable **Enforce HTTPS** if you want.

After that, the site will be live at **theincomeequation.com** and **www.theincomeequation.com**.
