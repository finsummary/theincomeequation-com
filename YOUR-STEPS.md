# What only you can do (no access from here)

Do these in order. Everything else is already done in the project.

---

## 1. Create the GitHub repo and push

- On GitHub: **New repository** (e.g. name: `theincomeequation-com`), **do not** add README/gitignore (repo should be empty).
- In this folder, run (replace `YOUR-USERNAME` and `YOUR-REPO`):

```bash
cd "c:\Users\user\Desktop\theincomeequation-com"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

---

## 2. Turn on GitHub Pages

- Repo → **Settings** → **Pages**
- **Source**: Deploy from a branch  
- **Branch**: `main`, folder **/ (root)**  
- **Save**

Site will be at `https://YOUR-USERNAME.github.io/YOUR-REPO/` until you add the custom domain.

---

## 3. Add your custom domain (Namecheap)

- In GitHub **Settings → Pages**: under **Custom domain**, type `theincomeequation.com` → **Save**.
- In **Namecheap**: Domain List → **Manage** for theincomeequation.com → **Advanced DNS**:
  - **A Record**: Host `@`, Value `185.199.108.153`  
    (optional: add more A records with `185.199.109.153`, `185.199.110.153`, `185.199.111.153`)
  - **CNAME Record**: Host `www`, Value `YOUR-USERNAME.github.io`
- Wait for DNS (up to 24–48 h), then in GitHub Pages enable **Enforce HTTPS** if you want.

---

## 4. Content (already done)

- **Substack**: Set to https://theincomeequation.substack.com/
- **Book text**: Your title, subtitle, and full description are in place.
- **Cover**: Your Canva cover is in `images/cover.png`. To update it later, replace that file and push.

---

That’s it. The rest (layout, CNAME, placeholder cover, git init and first commit) is already done.
