# Contributing to CodeGuard

First off, thank you for considering contributing to CodeGuard! 🎉

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues. When you create a bug report, include:

- **Clear title and description**
- **Steps to reproduce**
- **Expected behavior**
- **Actual behavior**
- **Screenshots** (if applicable)
- **Browser and OS version**

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Clear title and description**
- **Use case** - Why is this enhancement useful?
- **Possible implementation** (optional)

### Pull Requests

1. Fork the repo and create your branch from `main`
2. If you've added code, test it thoroughly
3. Ensure your code follows the existing style
4. Write clear commit messages
5. Update documentation if needed

## Code Style Guidelines

### JavaScript
- Use ES6+ features
- Use `const` and `let`, never `var`
- Use meaningful variable names
- Add comments for complex logic
- Follow existing formatting

### HTML/CSS
- Use semantic HTML5 tags
- Keep CSS organized by component
- Use consistent indentation (2 spaces)
- Mobile-first responsive design

## Adding New Language Support

To add a new programming language:

1. Add language option to `languageSelect` in HTML
2. Create analysis rules in `analysisRules` object:
```javascript
newlanguage: [
    {
        pattern: /your-regex-here/g,
        severity: 'critical|warning|info',
        title: 'Issue Title',
        description: 'Clear description of the issue',
        category: 'Category Name'
    },
    // More rules...
]
```

3. Test with sample code containing known issues
4. Update README.md with new language info

## Development Setup
```bash
# Clone your fork
git clone https://github.com/your-username/code-review-system.git

# Create a branch
git checkout -b feature/your-feature-name

# Make changes and test locally
python -m http.server 8000

# Commit and push
git add .
git commit -m "Description of changes"
git push origin feature/your-feature-name
```

## Testing

Before submitting a PR:
- [ ] Test with multiple browsers (Chrome, Firefox, Safari)
- [ ] Test with sample code for each supported language
- [ ] Verify mobile responsiveness
- [ ] Check console for errors
- [ ] Verify all links work

## Questions?

Feel free to open an issue with your question or reach out directly!

Thank you for contributing! 🚀
```