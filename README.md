
# README

Welcome to the content management guide for the Psychometrics and Data Science Laboratory website. This document will help you understand how to modify the contents of different pages, as well as how to add, modify, or delete profiles and projects.

**Note**: All content should be written in Markdown syntax. For a comprehensive guide on Markdown syntax, please refer to [Markdown Guide](https://www.markdownguide.org/).

## Home Page (`index.md`)

```markdown
---
layout: article
title: "Psychometrics<br>&nbsp;&nbsp;&nbsp;&nbsp;and<br>Data Science<br>Laboratory"
mode: immersive
header:
  theme: dark
article_header:
  type: overlay
  theme: dark
  background_color: '#123'
  background_image:
    src: /assets/bg.webp
excerpt: "directed by Professor J. Chen"
---
```

### Modifications
- **Title**: Change the title of the page. Note that HTML tags can be used for formatting.
- **Background Image**: Update the path to the background image (`background_image.src`) as needed.
- **Excerpt**: Modify the short description or tagline that appears on the home page.
- **Document Title**: The `<script>` section sets the document's title in the browser. Adjust this as necessary.

## About Page (`about.md`)

```markdown
---
layout: article
title: About
---
```

### Modifications
- **Content**: Update the welcome message, mission statement, and focus areas as necessary.
- **Images**: Change the path to the image to update the visual content.
- **Links**: Update the links in the footnotes to point to the correct profiles or resources.
- **Visitor Map**: Update the script source URL if the visitor map configuration changes.

## People Page (`people.md`)

```markdown
---
layout: articles
title: People
articles:
  data_source: site.people
  show_excerpt: true
  show_cover: true
  show_readmore: true
  excerpt_type: html
  show_info: false
  custom_order: [ "jinsong-chen" ]
---
```

### Modifications
- **Data Source**: Ensure `data_source` points to `site.people`.
- **Display Options**:
  - `show_excerpt`: Show or hide excerpts.
  - `show_cover`: Show or hide cover images.
  - `show_readmore`: Include or exclude "Read More" links.
  - `excerpt_type`: Define the type of excerpt (html/plain text).
  - `show_info`: Show or hide additional information like author and date.
- **Custom Order**: Specify the order of articles by listing the slugs in `custom_order`.

### Managing Profiles
- **Adding Profiles**: Create a new markdown file in the `site.people` directory with the necessary front matter and content. Example:
  ```markdown
  ---
  title: Professor Chen, Jinsong
  slug: jinsong-chen
  tags: People
  cover: /assets/people/jinsong-chen.jpg
  ---
  ```

- **Slug**: The `slug` is a URL-friendly version of the person's name. It should be unique for each person and is used as an identifier for ordering people on the People page. Make sure the `slug` matches the identifier used in the `custom_order` list in `people.md`.

- **Modifying Profiles**: Edit the markdown file of the person you want to modify in the `site.people` directory.
- **Deleting Profiles**: Remove the markdown file of the person from the `site.people` directory.

## Projects Page (`projects.md`)

```markdown
---
layout: articles
title: Projects
articles:
  data_source: site.projects
  show_excerpt: true
  show_cover: false
  show_readmore: true
  excerpt_type: html
  show_info: true
  reverse: true
---
```

### Modifications
- **Data Source**: Ensure `data_source` points to `site.projects`.
- **Display Options**:
  - `show_excerpt`: Show or hide excerpts.
  - `show_cover`: Show or hide cover images.
  - `show_readmore`: Include or exclude "Read More" links.
  - `excerpt_type`: Define the type of excerpt (html/plain text).
  - `show_info`: Show or hide additional information like author and date.
  - `reverse`: Display projects in reverse chronological order if set to true.

### Managing Projects
- **Adding Projects**: Create a new markdown file in the `site.projects` directory with the necessary front matter and content. Example:
  ```markdown
  ---
  title: "Advancing Generative AI in Personalized Learning"
  tags: Projects
  show_tags: false
  ---
  ```

- **Filename Format**: The filename for each project must follow the format `YYYY-MM-DD-Title-With-Hyphens.md`. The date should be in `YYYY-MM-DD` format, and the title should have spaces replaced with hyphens. Example: `2024-04-01-Advancing-Generative-AI-in-Personalized-Learning.md`.

- **Modifying Projects**: Edit the markdown file of the project you want to modify in the `site.projects` directory.
- **Deleting Projects**: Remove the markdown file of the project from the `site.projects` directory.

## Publications Page (`publications.md`)

```markdown
---
layout: article
title: Publications
---
```

### Modifications
- **Content**: Update the list of publications as necessary. Ensure that each publication entry includes the author's name, publication year, title, journal name, volume, and DOI.
- **Links**: Update the links to the profiles or external resources as needed.

## Courses Page (`courses.md`)

```markdown
---
layout: article
title: Courses
aside:
  toc: true
---
```

### Modifications
- **Content**: Update the list of courses, including course codes, titles, and instructors. Ensure the list is organized by year and semester.
- **Table of Contents**: The `toc` option in the `aside` section enables the table of contents. Set this to `false` if you do not want a TOC on this page.

## Resources Page (`resources.md`)

```markdown
---
layout: article
title: Resources
key: page-resources
---
```

### Modifications
- **Content**: Update the list of resources, including titles, links, authors, and descriptions. Add or remove resources as necessary.

---

This guide should help you manage the content on the Psychometrics and Data Science Laboratory website effectively. If you have any questions or need further assistance, please contact the website administrator.
