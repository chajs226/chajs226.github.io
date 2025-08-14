---
author: "Junseong Cha"
title: "Building a Multilingual Hugo Blog - Technical Notes"
date: "2025-08-14"
tags: 
- hugo
- multilingual
- technical
- notes
categories: ["notes"]
draft: false
---

## Technical Implementation Notes

### Hugo Configuration

The key to multilingual Hugo sites is proper configuration in `hugo.toml`:

```toml
defaultContentLanguage = 'ko'
defaultContentLanguageInSubdir = false

[languages]
  [languages.ko]
    languageCode = 'ko-kr'
    languageName = '한국어'
    title = "Junseong's Story"
    weight = 1
    
  [languages.en]
    languageCode = 'en-us'
    languageName = 'English'
    title = "Junseong's Story"
    weight = 2
```

### Content Structure

```
content/
├── ko/           # Korean content
│   ├── _index.md
│   ├── about.md
│   ├── posts/
│   └── notes/
└── en/           # English content
    ├── _index.md
    ├── about.md
    ├── posts/
    └── notes/
```

### URL Structure

- Korean (default): `/`, `/posts/`, `/notes/`, `/about/`
- English: `/en/`, `/en/posts/`, `/en/notes/`, `/en/about/`

### Language Switcher

Added to the header template with proper language detection and URL handling.

### Challenges Encountered

1. **Template Compatibility**: Had to modify header template for language switcher
2. **URL Routing**: Ensuring proper navigation between languages
3. **Menu Configuration**: Separate menus for each language

### Next Steps

- [ ] Add i18n translation files
- [ ] Implement proper translation linking
- [ ] Add hreflang tags for SEO
- [ ] Create translation workflow
