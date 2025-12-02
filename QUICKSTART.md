# Quick Start Guide

This is a quick reference for adding content to your Quarto website.

## Adding a New Blog Post

1. Create a new folder in `posts/` with the date and title:
   ```
   posts/2024-12-15-my-new-post/
   ```

2. Create an `index.qmd` file inside with this structure:
   ```yaml
   ---
   title: "My Blog Post Title"
   description: "A brief description"
   date: "2024-12-15"
   categories: [R, data science, visualization]
   ---
   
   ## Your Content Here
   
   Write your content using Markdown...
   ```

3. Add R code chunks for analysis:
   ````markdown
   ```{r}
   #| echo: true
   
   # Your R code here
   library(ggplot2)
   data(mtcars)
   ggplot(mtcars, aes(x = wt, y = mpg)) + geom_point()
   ```
   ````

## Adding a New Project

1. Create a new folder in `projects/` with your project name:
   ```
   projects/my-analysis/
   ```

2. Create an `index.qmd` file with:
   ```yaml
   ---
   title: "Project Title"
   description: "What this project is about"
   date: "2024-12-15"
   ---
   
   ## Overview
   
   Describe your project...
   ```

## Customizing Your Site

### Change Colors
Edit `custom.scss` and modify the `$primary` variable:
```scss
$primary: #2780e3 !default;  // Change to your preferred color
```

### Update Navigation
Edit `_quarto.yml` in the `navbar` section:
```yaml
navbar:
  right:
    - text: "New Page"
      href: newpage.qmd
```

### Change Personal Info
Update these files:
- `index.qmd` - Home page content
- `about.qmd` - About page content
- `contact.qmd` - Contact information
- `_quarto.yml` - Site title, footer, social links

## Preview Your Changes

```bash
quarto preview
```

## Build the Site

```bash
quarto render
```

## Publish to GitHub Pages

```bash
quarto publish gh-pages
```

## Tips

- All content files use `.qmd` extension (Quarto Markdown)
- R code chunks are executed when rendering
- Images can be added to `assets/` folder
- YAML front matter controls page metadata
- Use `#|` for code chunk options in R
