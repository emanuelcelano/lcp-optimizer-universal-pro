# Contributing to LCP Optimizer Universal PRO

First off, thank you for considering contributing to LCP Optimizer Universal PRO! 🎉

It's people like you that make this plugin better for everyone.

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Pull Requests](#pull-requests)
- [Development Setup](#development-setup)
- [Coding Guidelines](#coding-guidelines)
- [Commit Messages](#commit-messages)
- [Testing](#testing)

---

## 📜 Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

**Golden Rules:**
- Be respectful and inclusive
- Welcome newcomers
- Focus on constructive feedback
- Assume good intentions

---

## 🤝 How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check the [existing issues](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/issues) to avoid duplicates.

**When filing a bug report, include:**

```markdown
**Environment:**
- WordPress Version: [e.g., 6.4.2]
- PHP Version: [e.g., 8.1]
- Plugin Version: [e.g., 2.3.2]
- Theme: [e.g., Astra 4.0]
- Active Plugins: [list major plugins like WP Rocket, Elementor]

**Steps to Reproduce:**
1. Go to '...'
2. Click on '...'
3. See error

**Expected Behavior:**
A clear description of what you expected to happen.

**Actual Behavior:**
What actually happened.

**Screenshots:**
If applicable, add screenshots.

**Additional Context:**
Any other relevant information.
```

Use the bug report template: [Create Bug Report →](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/issues/new?template=bug_report.md)

---

### 💡 Suggesting Enhancements

Enhancement suggestions are tracked as [GitHub issues](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/issues).

**When suggesting an enhancement, include:**

```markdown
**Is your feature request related to a problem?**
A clear description of the problem. E.g., "I'm always frustrated when..."

**Describe the solution you'd like**
A clear description of what you want to happen.

**Describe alternatives you've considered**
Any alternative solutions or features you've considered.

**Additional context**
Any other context, screenshots, or examples.

**Would you be willing to implement this?**
[ ] Yes, I can submit a PR
[ ] No, but I can help test
[ ] No, just suggesting
```

Use the feature request template: [Request Feature →](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/issues/new?template=feature_request.md)

---

### 🔧 Pull Requests

**Process:**

1. **Fork** the repository
2. **Create** a feature branch:
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. **Make** your changes
4. **Test** thoroughly (see [Testing](#testing))
5. **Commit** using conventional commits (see [Commit Messages](#commit-messages))
6. **Push** to your fork:
   ```bash
   git push origin feature/YourFeatureName
   ```
7. **Open** a Pull Request

**PR Guidelines:**

- ✅ One feature/fix per PR
- ✅ Update documentation if needed
- ✅ Add tests if applicable
- ✅ Follow coding standards
- ✅ Keep commits clean and atomic
- ✅ Reference related issues

**PR Template:**

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix (non-breaking change fixing an issue)
- [ ] New feature (non-breaking change adding functionality)
- [ ] Breaking change (fix/feature causing existing functionality to break)
- [ ] Documentation update

## Testing
How you tested this change

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-reviewed the code
- [ ] Commented hard-to-understand areas
- [ ] Updated documentation
- [ ] No new warnings generated
- [ ] Added tests (if applicable)
- [ ] All tests pass locally

## Screenshots (if applicable)
Add screenshots to demonstrate changes
```

---

## 💻 Development Setup

### Prerequisites

- PHP 7.4+ (8.0+ recommended)
- WordPress 6.0+
- Node.js 16+ (for development tools)
- Git

### Setup Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/emanuelcelano/lcp-optimizer-universal-pro.git
   cd lcp-optimizer-universal-pro
   ```

2. **Install to WordPress:**
   ```bash
   # Copy to WordPress plugins directory
   cp -r . /path/to/wordpress/wp-content/plugins/lcp-optimizer-universal-pro/
   ```

3. **Activate plugin** in WordPress admin

4. **Enable debug mode** in `wp-config.php`:
   ```php
   define('WP_DEBUG', true);
   define('WP_DEBUG_LOG', true);
   define('WP_DEBUG_DISPLAY', false);
   ```

---

## 📝 Coding Guidelines

### PHP Standards

Follow [WordPress Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/):

```php
<?php
/**
 * Function description
 *
 * @param string $param Description
 * @return bool Description
 */
function lcp_optimizer_function_name( $param ) {
    if ( ! $param ) {
        return false;
    }
    
    return true;
}
```

**Key Points:**
- Use WordPress naming conventions (`function_name` not `functionName`)
- Sanitize all inputs
- Escape all outputs
- Use nonces for forms
- Follow security best practices

### JavaScript Standards

```javascript
/**
 * Function description
 * @param {string} param - Description
 * @returns {boolean} Description
 */
function lcpOptimizerFunction(param) {
    if (!param) {
        return false;
    }
    
    return true;
}
```

**Key Points:**
- Use ES6+ features
- No jQuery dependency
- Comment complex logic
- Keep functions small and focused

### CSS Standards

```css
/* Component: Button */
.lcp-optimizer-button {
    padding: 10px 20px;
    background: #007cba;
}

.lcp-optimizer-button:hover {
    background: #005a87;
}
```

**Key Points:**
- Use BEM-like naming
- Prefix all classes with `lcp-optimizer-`
- Mobile-first approach
- Keep specificity low

---

## 📝 Commit Messages

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no logic change)
- `refactor`: Code refactoring
- `test`: Adding/updating tests
- `chore`: Maintenance tasks

**Examples:**

```bash
feat(fonts): add Google Fonts CSS URL field

Added manual control for Google Fonts URL in settings.
Includes performance tip about font weights.

Closes #123
```

```bash
fix(menu): resolve dropdown menu flashing issue

Fixed CSS timing issue causing menu flash on page load.
Added safeguards for theme compatibility.

Fixes #456
```

---

## 🧪 Testing

### Manual Testing Checklist

Before submitting a PR, test:

- [ ] Clean WordPress 6.0+ installation
- [ ] With popular themes (Astra, GeneratePress, Divi)
- [ ] With Elementor/Elementor Pro
- [ ] With WP Rocket enabled
- [ ] With WP_DEBUG enabled (no errors)
- [ ] On PHP 7.4, 8.0, and 8.1
- [ ] Performance (PageSpeed Insights, GTmetrix)

### Testing Tools

```bash
# Run PageSpeed test
curl "https://www.googleapis.com/pagespeedonline/v5/runPagespeed?url=YOUR_SITE"

# Check PHP syntax
php -l lcp-optimizer-universal-pro.php
```

### Performance Testing

1. Test **before** your changes:
   - PageSpeed Insights score
   - LCP, INP, CLS values
   - GTmetrix grade

2. Test **after** your changes:
   - Compare scores
   - Document improvements
   - Check for regressions

---

## 📚 Documentation

When adding new features:

1. **Update README.md** with feature description
2. **Update CHANGELOG.md** with version changes
3. **Add inline comments** for complex code
4. **Update wiki** if needed (coming soon)

---

## 🏷️ Versioning

We use [Semantic Versioning](https://semver.org/):

- **MAJOR** version for incompatible changes (e.g., 2.0.0 → 3.0.0)
- **MINOR** version for new features (e.g., 2.3.0 → 2.4.0)
- **PATCH** version for bug fixes (e.g., 2.3.1 → 2.3.2)

---

## 🙏 Recognition

Contributors will be recognized in:
- README.md Contributors section
- CHANGELOG.md for their contributions
- Release notes

---

## 📧 Questions?

- **GitHub Discussions:** [Ask a question](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/discussions)
- **Email:** info@analisideirischinformatici.it

---

Thank you for contributing to making WordPress faster! 🚀

**Made with ❤️ by the community**
