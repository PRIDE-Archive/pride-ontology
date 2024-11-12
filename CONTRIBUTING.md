# Contribution Guidelines

Thank you for your interest in contributing to this ontology repository! We welcome contributions to improve, expand, and refine the ontology. Please review the following guidelines to help ensure a smooth and effective collaboration.

## Table of Contents
1. [Overview](#overview)
2. [Getting Started](#getting-started)
3. [Ontology Contribution Guidelines](#ontology-contribution-guidelines)
4. [Creating Issues](#creating-issues)
5. [Submitting Pull Requests](#submitting-pull-requests)
6. [Code of Conduct](#code-of-conduct)
7. [License](#license)

---

### 1. Overview

The PRIDE ontology repository is designed to provide a structured vocabulary for [PRIDE database]. Contributors are encouraged to add new terms, improve definitions, or report issues to help the ontology remain relevant and accurate.

### 2. Getting Started

1. **Fork the repository**: First, fork this repository to your own GitHub account.
2. **Clone the repository**: Clone your fork to your local development environment.
    ```bash
    git clone https://github.com/{your-user}/pride-ontology
    ```
3. **Set up the environment** (if applicable): Follow any environment setup instructions provided in the repository to ensure compatibility with the tools and software used to manage the ontology.
4. **Review existing terms**: Familiarize yourself with the ontology structure and existing terms before making changes.

### 3. Ontology Contribution Guidelines

**IMPORTANT NOTE**: All contributions should be done in the file: [pride_cv.obo](pride_cv.obo)

To maintain consistency and quality, please follow these guidelines when contributing to the ontology:

#### Adding a New Term
- **Check for duplicates**: Before adding a new term, search the ontology to ensure it isn’t already defined.
- **Use clear, descriptive names**: Term names should be concise yet descriptive.
- **Provide a definition**: Each term should have a precise definition. Avoid jargon and keep it as clear as possible.
- **Add relationships**: If applicable, specify the term’s relationships to other terms (e.g., `is_a`, `part_of`, `related_to`).
- **Include references**: If your term or definition is derived from a specific source, cite it in the term metadata.

#### Modifying an Existing Term
- **Explain the reason for changes**: Clearly explain why you are modifying a term, either as a comment in the pull request or in the ontology file if supported.
- **Preserve existing relationships**: Avoid breaking relationships unless there is a compelling reason. Any change should be documented.

### 4. Creating Issues

If you encounter a bug, error, or want to suggest a new feature or term:

1. **Check for existing issues**: Search the [Issues](https://github.com/PRIDE-Archive/pride-ontology/issues) page to see if the topic has already been discussed.
2. **Create a new issue**: If it hasn’t been addressed, open a new issue. 
3. **Provide detailed information**: Describe the issue clearly, providing as much context as possible. Include:
    - A descriptive title
    - Steps to reproduce (if applicable)
    - Expected vs. actual behavior
    - Screenshots, examples, or other supporting information, if relevant
4. **Label the issue**: Use appropriate labels (e.g., `bug`, `enhancement`, `new term`) to help categorize the issue.

### 5. Submitting Pull Requests

Once you’ve made your changes, you can submit a pull request (PR) for review:

1. **Ensure all changes are committed**: Stage and commit your changes with a descriptive commit message.
2. **Push to your fork**: Push the changes to your forked repository.
3. **Open a pull request**: Go to the original repository, select your fork, and open a pull request. 
4. **Describe your changes**: In the pull request description, include:
    - The reason for the changes
    - Links to any related issues or discussions
    - Any potential impacts of the change on existing terms or users
5. **Request a review**: Tag a maintainer if a specific review is needed, and wait for feedback.
6. **Respond to feedback**: Be prepared to make adjustments based on feedback from maintainers.

### 7. License

By contributing, you agree that your contributions will be licensed under the same license as the repository. See the [LICENSE](LICENSE) file for more information.

---

Thank you for contributing to our ontology repository!

