# CodeGuard - Usage Guide

## Getting Started

### Step 1: Access the Tool
Visit [https://SawwmyaP.github.io/code-review-system/](https://SawwmyaP.github.io/code-review-system/)

### Step 2: Prepare Your Code
Copy the code you want to analyze to your clipboard.

### Step 3: Select Language
Choose the appropriate programming language from the dropdown menu.

### Step 4: Paste and Analyze
- Paste your code into the text area
- Click the "🔍 Analyze Code" button
- Or use keyboard shortcut: `Ctrl + Enter`

## Understanding Results

### Quality Score
- **Color Indicators:**
  - Green (90-100): Excellent code quality
  - Yellow (70-89): Good, minor improvements
  - Orange (50-69): Needs attention
  - Red (0-49): Critical issues

### Issue Severity Levels

**🔴 Critical**
- Security vulnerabilities
- Logic bugs that will cause crashes
- Data loss risks
- Immediate action required

**🟡 Warning**
- Code smells
- Maintainability issues
- Best practice violations
- Should be addressed

**🔵 Info**
- Style suggestions
- Minor improvements
- Educational notes
- Nice-to-have fixes

## Best Practices

### Before Analyzing
1. Remove sensitive data (passwords, API keys)
2. Ensure code is properly formatted
3. Include enough context for analysis

### After Analysis
1. Address Critical issues first
2. Review Warnings and decide priority
3. Learn from Info suggestions
4. Re-analyze after fixes

## Examples

### JavaScript Example
```javascript
// Bad code (will detect issues)
function getData(id) {
    var url = "api.com/" + id;
    if(id == null) {  // Should use ===
        console.log("No ID");  // Remove in production
        eval(url);  // Security risk!
    }
}

// Good code (after fixes)
function getData(id) {
    const url = `api.com/${id}`;
    if(id === null) {
        // Handle error properly
        throw new Error("ID is required");
    }
    return fetch(url);
}
```

### Python Example
```python
# Bad code
def process():
    try:
        from module import *  # Wildcard import
        result = exec(code)  # Security risk
    except:  # Bare except
        pass

# Good code
def process():
    from module import specific_function
    try:
        result = safe_execute(code)
    except ValueError as e:
        logger.error(f"Processing failed: {e}")
        raise
```

## FAQ

**Q: Is my code sent to a server?**
A: No! All analysis happens locally in your browser. Your code never leaves your machine.

**Q: Can I analyze multiple files?**
A: Currently, it analyzes one file at a time. Copy and paste each file separately.

**Q: Why isn't my language supported?**
A: We're constantly adding languages! Submit a feature request on GitHub.

**Q: Can I customize the rules?**
A: Not yet, but this feature is planned for version 2.0.

**Q: How accurate is the analysis?**
A: Pattern-based detection is very accurate for common issues. However, it may miss context-specific problems that require deeper semantic analysis.

## Tips & Tricks

1. **Test with Known Bugs**: Try analyzing code with deliberate bugs to see how the tool detects them
2. **Learn as You Go**: Read the descriptions to understand why something is flagged
3. **Incremental Fixes**: Fix issues one at a time and re-analyze
4. **Save Good Code**: Keep examples of clean code for reference

## Keyboard Shortcuts

- `Ctrl + Enter` - Analyze code
- `Escape` - Clear input (coming soon)

## Need Help?

- 📧 Email: pathaksoumya2005@gmail.com
- 🐛 Report bugs: [GitHub Issues](https://github.com/SawwmyaP/code-review-system/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/SawwmyaP/code-review-system/discussions)