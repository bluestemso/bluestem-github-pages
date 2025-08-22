# Setting Up Your New GitHub Repository

This guide will help you create a fresh GitHub repository for your Bluestem project, removing all traces of the original fork.

## Step 1: Remove Existing Git History

Since this is a forked template, you need to remove the existing git history:

```bash
# Navigate to your project directory
cd /Users/tschaack/Developer/localProjects/bluestem-github-pages

# Remove the existing git repository
rm -rf .git

# Remove any existing git remotes (if any)
git remote remove origin
```

## Step 2: Create a New GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name it something like `bluestem-website` or `bluestem-github-pages`
5. Make it public (for GitHub Pages) or private (your choice)
6. **DO NOT** initialize with README, .gitignore, or license (we already have these)
7. Click "Create repository"

## Step 3: Initialize New Git Repository

```bash
# Initialize a new git repository
git init

# Add all files
git add .

# Make your first commit
git commit -m "Initial commit: Bluestem website setup"

# Add your new GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 4: Enable GitHub Pages

1. Go to your new repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" section
4. Under "Source", select "GitHub Actions"
5. The GitHub Actions workflow will automatically deploy your site

## Step 5: Customize Your Site

Update the following files to personalize your site:

- `_config.yml` - Site title, description, contact info, social links
- `index.md` - Homepage content
- `landing.md` - Landing page content
- `_posts/` - Add your own blog posts
- `assets/images/` - Replace with your own images

## Step 6: Test Locally (Optional)

To test your site locally before pushing:

```bash
# Install dependencies
bundle install

# Run the site locally
bundle exec jekyll serve

# Open http://localhost:4000 in your browser
```

## Important Notes

- The site will be available at `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME`
- If you want it at `https://YOUR_USERNAME.github.io`, rename your repository to `YOUR_USERNAME.github.io`
- The GitHub Actions workflow will automatically rebuild and deploy your site on every push
- Make sure your repository is public for GitHub Pages to work

## Next Steps

After setting up your repository:
1. Customize the content in `_config.yml`
2. Replace placeholder images in `assets/images/`
3. Update the homepage content in `index.md`
4. Add your own blog posts in `_posts/`
5. Customize the styling in `_sass/` if needed
