# Bluestem

This site is built using Jekyll and deployed on Github Pages.

## Getting Started

### Prerequisites
- Ruby (version 2.5.0 or higher)
- Bundler (`gem install bundler`)

### Local Development
1. Install dependencies:
   ```bash
   bundle install
   ```

2. Run the site locally:
   ```bash
   bundle exec jekyll serve
   ```
   The site will be available at `http://localhost:4000`

## Creating New Posts

1. Create a new file in the `_posts` directory with the following naming convention:
   ```
   YYYY-MM-DD-title-of-your-post.md
   ```

2. Add the following front matter at the top of your post:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD HH:MM:SS +/-TTTT
   categories: [category1, category2]
   ---
   ```

3. Write your content below the front matter using Markdown syntax.

## Customizing the Site

### Changing the Look and Feel

1. **Layouts**: Modify files in the `_layouts` directory to change the structure of your pages
   - `default.html`: The base layout for all pages
   - `post.html`: The layout for blog posts

2. **Styles**: 
   - CSS files are typically located in the `assets/css` directory
   - Modify these files to change colors, fonts, and other visual elements

3. **Configuration**:
   - Edit `_config.yaml` to change site-wide settings like:
     - Site title and description
     - Base URL
     - Default layout
     - Theme settings

### Adding Pages

1. Create new `.md` or `.html` files in the root directory
2. Add front matter at the top of each file:
   ```yaml
   ---
   layout: default
   title: "Your Page Title"
   ---
   ```

## Deployment

The site is automatically deployed to GitHub Pages when you push changes to the main branch. No additional steps are required.

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)

