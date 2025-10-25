# 🛡️ CodeGuard - Intelligent Code Review System

<div align="center">

![CodeGuard Banner](https://img.shields.io/badge/CodeGuard-Intelligent%20Review-blueviolet?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-success?style=for-the-badge)

**An autonomous code review and bug detection system that analyzes code across multiple programming languages in real-time.**

[🚀 Live Demo](https://yourusername.github.io/code-review-system/) | [📖 Documentation](docs/USAGE.md) | [🐛 Report Bug](https://github.com/yourusername/code-review-system/issues)

</div>

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Live Demo](#live-demo)
- [Supported Languages](#supported-languages)
- [What It Detects](#what-it-detects)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Metrics Explained](#metrics-explained)
- [Screenshots](#screenshots)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 About

CodeGuard is an intelligent, browser-based code analysis tool designed to help developers identify bugs, security vulnerabilities, and code quality issues before they make it to production. Built with vanilla JavaScript, it requires no backend and runs entirely in your browser.

**Why CodeGuard?**
- ✅ **Instant Analysis** - No setup, no installation
- ✅ **Multi-Language Support** - Works with 7+ programming languages
- ✅ **Educational** - Learn best practices as you code
- ✅ **Privacy-First** - All analysis happens locally in your browser
- ✅ **Portfolio Ready** - Clean, professional design

---

## 🚀 Features

### Core Functionality
- **🔍 Real-Time Code Analysis** - Instant feedback as you paste code
- **🐛 Bug Detection** - Identifies logic errors, off-by-one errors, and common mistakes
- **🔒 Security Scanning** - Detects dangerous functions and vulnerabilities
- **📊 Quality Metrics** - Code quality score, complexity analysis, and LOC counting
- **⚡ Performance Optimized** - Fast pattern matching and analysis
- **🎨 Beautiful UI** - Modern gradient design with smooth animations

### Detailed Analysis
- **Severity Levels**: Critical, Warning, Info
- **Issue Categories**: Security, Bug, Best Practice, Maintainability, Design
- **Line-Level Detection**: Shows exactly where issues occur
- **Actionable Suggestions**: Clear recommendations for fixes

---

## 🌐 Live Demo

**Try it now:** [https://yourusername.github.io/code-review-system/](https://yourusername.github.io/code-review-system/)

No installation required - just open and start analyzing!

---

## 💻 Supported Languages

<table>
  <tr>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="50px" />
      <br />JavaScript
    </td>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="50px" />
      <br />Python
    </td>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="50px" />
      <br />Java
    </td>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="50px" />
      <br />CSS
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="50px" />
      <br />HTML
    </td>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" width="50px" />
      <br />C++
    </td>
    <td align="center">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" width="50px" />
      <br />C#
    </td>
    <td align="center">
      <strong>+</strong>
      <br />More Soon
    </td>
  </tr>
</table>

---

## 🔎 What It Detects

### JavaScript
- ❌ Use of `var` instead of `let`/`const`
- ❌ Loose equality operators (`==` vs `===`)
- ❌ Console.log statements (production code)
- ⚠️ **Critical**: `eval()` usage (security risk)
- ⚠️ **Critical**: Array index out of bounds
- ⚠️ Functions exceeding recommended length

### Python
- ❌ Bare `except:` clauses
- ❌ Wildcard imports (`from x import *`)
- ❌ Incorrect None comparisons (`== None` vs `is None`)
- ⚠️ **Critical**: `exec()` usage (security risk)
- ⚠️ Overly long functions

### Java
- ❌ `System.out.println()` in production code
- ❌ Empty catch blocks
- ❌ Classes violating Single Responsibility Principle
- ❌ Null comparisons (suggest Optional)

### CSS
- ❌ Overuse of `!important`
- ❌ Fixed pixel widths (responsive design)
- ⚠️ Color values without fallbacks

### HTML
- ⚠️ Images without `alt` attributes (accessibility)
- ❌ Inline event handlers
- ⚠️ Inline styles (maintainability)

---

## 🛠️ Technologies Used

- **HTML5** - Semantic structure
- **CSS3** - Modern gradients, flexbox, grid, animations
- **JavaScript (ES6+)** - Regex pattern matching, DOM manipulation
- **GitHub Pages** - Free hosting
- **No Dependencies** - Pure vanilla JavaScript

---

## 🏁 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for initial load only)

### Installation

**Option 1: Use Online (Recommended)**
```
Simply visit: https://yourusername.github.io/code-review-system/
```

**Option 2: Run Locally**
```bash
# Clone the repository
git clone https://github.com/yourusername/code-review-system.git

# Navigate to project directory
cd code-review-system

# Open in browser
open index.html
# or
python -m http.server 8000  # Then visit http://localhost:8000
```

---

## 📖 Usage

### Quick Start
1. **Paste Code** - Copy your code into the text area
2. **Select Language** - Choose from the dropdown menu
3. **Analyze** - Click "🔍 Analyze Code" button
4. **Review Results** - Check issues and metrics

### Keyboard Shortcuts
- `Ctrl + Enter` - Analyze code
- `Escape` - Clear results

### Example Test Cases

**JavaScript Test (with bugs):**
```javascript
function calculateTotal(items) {
    var total = 0;
    for(var i = 0; i <= items.length; i++) {
        total += items[i].price;
    }
    return total;
}
```

**Python Test (with bugs):**
```python
def process_data(data):
    try:
        result = eval(data)
        return result
    except:
        pass
```

---

## 📊 Metrics Explained

### Code Quality Score (0-100)
- **90-100**: Excellent - Very few issues
- **70-89**: Good - Minor improvements needed
- **50-69**: Fair - Several issues to address
- **0-49**: Needs Work - Critical issues present

**Calculation:**
```
Score = 100 - (Issues × 5) - (Complexity Penalty × 2)
```

### Cyclomatic Complexity
Measures code complexity based on decision points:
- **1-10**: Simple, easy to maintain
- **11-20**: Moderate complexity
- **21+**: High complexity, consider refactoring

### Lines of Code (LOC)
Non-empty lines analyzed (excludes blank lines)

---

## 📸 Screenshots

### Main Interface
![Main Interface](docs/screenshots/main-interface.png)

### Analysis Results
![Analysis Results](docs/screenshots/analysis-results.png)

### Issue Detection
![Issue Detection](docs/screenshots/issue-detection.png)

---

## 🗺️ Roadmap

### Version 2.0 (Planned)
- [ ] AI-powered fix suggestions using GPT
- [ ] Custom rule configuration
- [ ] Export reports as PDF/Markdown
- [ ] Dark/Light theme toggle
- [ ] Code formatting suggestions

### Version 3.0 (Future)
- [ ] GitHub API integration
- [ ] Multi-file project analysis
- [ ] CI/CD pipeline integration
- [ ] VS Code extension
- [ ] Support for TypeScript, Rust, Go, Ruby

---

## 🤝 Contributing

Contributions are what make the open-source community amazing! Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## 📄 License

Distributed under the MIT License. See [LICENSE](LICENSE) for more information.

---

## 👨‍💻 Contact

Your Name - [@yourtwitter](https://twitter.com/yourtwitter) - your.email@example.com

Project Link: [https://github.com/yourusername/code-review-system](https://github.com/yourusername/code-review-system)

---

## 🙏 Acknowledgments

- Inspired by modern linting tools like ESLint and Pylint
- Design inspiration from GitHub and VS Code
- Icons and badges from [Shields.io](https://shields.io)
- Devicon for language icons

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

Made with ❤️ by [Your Name](https://github.com/yourusername)

</div>
```

---

## **3. LICENSE**
```
MIT License

Copyright (c) 2025 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.