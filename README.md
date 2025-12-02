# conor-o-driscoll.github.io

The personal website of Dr. Conor O'Driscoll.

## About This Website

This website is built using [Quarto](https://quarto.org), an R-based publishing system that allows you to create websites without writing HTML. The template mimics the aesthetic structure of [Silvia Canelón's website](https://github.com/spcanelon/silvia) while keeping the implementation minimal and R-focused.

## Prerequisites

To work with this website, you need:

- [R](https://www.r-project.org/) (version 4.0 or higher)
- [Quarto](https://quarto.org/docs/get-started/) (version 1.4 or higher)

## Getting Started

### Preview the Website Locally

To preview the website on your local machine:

```bash
quarto preview
```

This will start a local server and open the website in your browser. The preview will automatically update as you make changes.

### Render the Website

To build the website:

```bash
quarto render
```

The rendered website will be in the `_site` directory.

### Publish to GitHub Pages

To publish your website to GitHub Pages:

```bash
quarto publish gh-pages
```

## Customization

### Updating Content

- **Home Page**: Edit `index.qmd`
- **About Page**: Edit `about.qmd`
- **Projects**: Edit `projects.qmd` and add project files in a `projects/` directory
- **Blog**: Edit `blog.qmd` and add blog posts in a `posts/` directory
- **Contact**: Edit `contact.qmd`

### Styling

- Basic styling is controlled in `custom.scss`
- Main configuration is in `_quarto.yml`

### Navigation

Edit the `navbar` section in `_quarto.yml` to add or remove navigation items.

## Project Structure

```
.
├── _quarto.yml          # Main configuration file
├── index.qmd            # Home page
├── about.qmd            # About page
├── projects.qmd         # Projects page
├── blog.qmd             # Blog listing page
├── contact.qmd          # Contact page
├── custom.scss          # Custom styling
└── README.md            # This file
```

## Adding Content with R

You can add R code and visualizations to any `.qmd` file using code chunks:

````markdown
```{r}
# Your R code here
library(ggplot2)
ggplot(mtcars, aes(x = wt, y = mpg)) + 
  geom_point()
```
````

## License

This project is licensed under the terms specified in the LICENSE file.
