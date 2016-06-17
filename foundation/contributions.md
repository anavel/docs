# Contribution Guide

- [Bug Reports](#bug-reports)
- [Core Development Discussion](#core-development-discussion)
- [Which Branch?](#which-branch)
- [Security Vulnerabilities](#security-vulnerabilities)
- [Coding Style](#coding-style)

### <a name="bug-reports"></a> Bug Reports

To encourage active collaboration, we strongly encourages pull requests, not just bug reports. "Bug reports" may also be sent in the form of a pull request containing a failing test.

However, if you file a bug report, your issue should contain a title and a clear description of the issue. You should also include as much relevant information as possible and a code sample that demonstrates the issue. The goal of a bug report is to make it easy for yourself - and others - to replicate the bug and develop a fix.

Remember, bug reports are created in the hope that others with the same problem will be able to collaborate with you on solving it. Do not expect that the bug report will automatically see any activity or that others will jump to fix it. Creating a bug report serves to help yourself and others start on the path of fixing the problem.

The Anavel source code is managed on Github, and there are repositories for each of the Anavel official projects:

- [Foundation](https://github.com/anavel/foundation)
- [CRUD](https://github.com/anavel/crud)
- [Gettext](https://github.com/anavel/gettext)
- [Translation](https://github.com/anavel/translation)
- [Uploads](https://github.com/anavel/uploads)
- [Anavel Website](https://github.com/anavel/anavel.org)

### <a name="core-development-discussion"></a> Core Development Discussion

You may propose general new features or improvements of existing Anavel behavior in the Anavel Foundation [issue board](https://github.com/anavel/foundation/issues). If you know the specific project for which you may propose, you can use the project issue board. If you propose a new feature, please be willing to implement at least some of the code that would be needed to complete the feature.

### <a name="which-branch"></a> Which Branch?

### <a name="security-vulnerabilities"></a> Security Vulnerabilities

If you discover a security vulnerability within Anavel, please send an e-mail to idc@anavallasuiza.com. All security vulnerabilities will be promptly addressed.

### <a name="coding-style"></a> Coding Style

Anavel follows the [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) coding standard and the [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md) autoloading standard.

If your code style isn't perfect, don't worry! StyleCI will automatically PR any style fixes into the Anavel repository after any pull requests are merged. This allows us to focus on the content of the contribution and not the code style.
