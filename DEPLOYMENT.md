# Deploying Immaculate Vibes Landing Page to GitHub Pages

This guide will help you deploy your Immaculate Vibes landing page to GitHub Pages for free hosting.

## Prerequisites

- A GitHub account
- Git installed on your computer
- Your landing page files (index.html, styles.css, and image files)

## Step 1: Create a New GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in to your account
2. Click the "+" icon in the top right corner and select "New repository"
3. Name your repository `immaculate-vibes` (or any name you prefer)
4. Make sure the repository is set to **Public** (required for free GitHub Pages)
5. Check "Add a README file"
6. Click "Create repository"

## Step 2: Clone the Repository Locally

1. On your repository page, click the green "Code" button
2. Copy the HTTPS URL (it will look like: `https://github.com/yourusername/immaculate-vibes.git`)
3. Open your terminal/command prompt
4. Navigate to where you want to store the project
5. Run: `git clone https://github.com/yourusername/immaculate-vibes.git`
6. Navigate into the folder: `cd immaculate-vibes`

## Step 3: Add Your Website Files

1. Copy your website files into the cloned repository folder:
   - `index.html`
   - `styles.css`
   - `james.jpeg`
   - `mel.png`

2. Add and commit the files:
   ```bash
   git add .
   git commit -m "Add Immaculate Vibes landing page"
   git push origin main
   ```

## Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on the "Settings" tab (not your account settings, but the repository settings)
3. Scroll down to the "Pages" section in the left sidebar
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click "Save"

## Step 5: Access Your Live Website

1. GitHub will provide you with a URL like: `https://yourusername.github.io/immaculate-vibes/`
2. It may take a few minutes for the site to go live
3. You can find the URL in the "Pages" section of your repository settings

## Step 6: Set Up Google Form for Waitlist

1. Go to [Google Forms](https://forms.google.com)
2. Create a new form with the following fields:
   - Full Name (Short answer, Required)
   - Email Address (Short answer, Required, with email validation)
   - How did you hear about us? (Multiple choice: Social Media, Word of Mouth, Search Engine, Other)
   - What are you hoping to build? (Paragraph, Optional)
   - Any questions for us? (Paragraph, Optional)

3. Configure the form:
   - Set the title to "Immaculate Vibes AI Bootcamp - Waitlist"
   - Add a description: "Join the waitlist for our next AI bootcamp cohort starting September 8th!"
   - Enable "Collect email addresses" in settings
   - Set up email notifications for new responses

4. Get the embed code:
   - Click the "Send" button in your form
   - Click the embed icon `<>`
   - Copy the iframe code
   - Replace the placeholder iframe in your `index.html` file with the actual embed code

## Step 7: Update Your Website with the Real Google Form

1. Edit your `index.html` file
2. Find the line with `src="https://docs.google.com/forms/d/e/1FAIpQLSfYourFormIDHere/viewform?embedded=true"`
3. Replace it with your actual Google Form embed URL
4. Also update the fallback link in the same section
5. Save and push the changes:
   ```bash
   git add index.html
   git commit -m "Add real Google Form for waitlist"
   git push origin main
   ```

## Updating Your Website

Whenever you make changes to your website:

1. Edit the files locally
2. Save your changes
3. Add, commit, and push to GitHub:
   ```bash
   git add .
   git commit -m "Description of your changes"
   git push origin main
   ```
4. Changes will automatically appear on your live website within a few minutes

## Custom Domain (Optional)

If you want to use a custom domain like `immaculatevibes.com`:

1. Purchase a domain from a provider like Namecheap, GoDaddy, or Cloudflare
2. In your repository, create a file named `CNAME` (no extension) in the root folder
3. Add your domain name as the only content in the file (e.g., `immaculatevibes.com`)
4. In your domain provider's DNS settings, add a CNAME record pointing to `yourusername.github.io`
5. In your GitHub repository settings > Pages, enter your custom domain and enable "Enforce HTTPS"

## Troubleshooting

**Website not loading?**
- Make sure your main file is named `index.html` (case sensitive)
- Check that the repository is public
- Wait a few minutes after enabling GitHub Pages

**Form not working?**
- Make sure you've replaced the placeholder Google Form URL with your actual form URL
- Test the form directly in Google Forms first
- Check that the form is set to accept responses

**Images not showing?**
- Make sure image files are uploaded to the repository
- Check that image file names match exactly (case sensitive)
- Verify image paths in your HTML

## Need Help?

If you run into issues:
1. Check the GitHub Pages documentation: https://docs.github.com/en/pages
2. Make sure all files are properly committed and pushed to the main branch
3. Check the "Actions" tab in your GitHub repository for any deployment errors

Your Immaculate Vibes landing page should now be live and ready to collect waitlist signups!