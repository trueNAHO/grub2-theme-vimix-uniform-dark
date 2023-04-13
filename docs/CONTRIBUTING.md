# Contributing

Thank you for considering contributing to this project! We appreciate any
contribution you can make to this project, whether it's reporting a bug,
requesting a feature, improving the code, or polishing the documentation. To
ensure that everything runs smoothly, please review the guidelines below before
submitting your contribution.

<!--toc:start-->
- [What We Want](#what-we-want)
- [What We Do Not Want](#what-we-do-not-want)
- [Contribution Guidelines](#contribution-guidelines)
  - [How to Submit Changes](#how-to-submit-changes)
  - [Commit Standards](#commit-standards)
  - [Tests](#tests)
  - [Modify the `theme.txt` file](#modify-the-themetxt-file)
  - [Add Icons](#add-icons)
  - [Add Fonts](#add-fonts)
- [Code of Conduct](#code-of-conduct)
- [License](#license)
<!--toc:end-->

## What We Want

We welcome any contributions that help improve this project. Here are some
examples of the kinds of contributions we are looking for:

- Bug reports and feature requests
- Code improvements and bug fixes
- Documentation improvements
- Expanding the collection of distribution logos to cover a wider range of
  distributions.
- Additional theme variations that do not deviate too much from the original
  look and feel, such as modifications to the background, color scheme, or font.

If you are uncertain about whether your contribution aligns with the scope of
this project, please refer to the [What We Do Not Want](#what-we-do-not-want)
section. Feel free to reach out to the maintainers, if you have any questions.

## What We Do Not Want

While we appreciate all contributions that help improve this project, some may
not align with our vision, require further discussion, or may be better suited
for a fork. Here are some examples that may fall into this category:

- Drastic modifications to the overall look and feel of the theme
- Compatibility breaking changes

If you are uncertain about whether your contribution aligns with the scope of
this project, please refer to the [What We Want](#what-we-want) section. Feel
free to reach out to the maintainers, if you have any questions.

## Contribution Guidelines

Contributions to this project are welcome! To ensure consistency and quality,
please adhere to the following guidelines when submitting changes:

### How to Submit Changes

To submit changes to this repository, please follow [these
steps](https://docs.github.com/en/get-started/quickstart/contributing-to-projects):

- [Fork the
  repository](https://docs.github.com/en/get-started/quickstart/contributing-to-projects#forking-a-repository)
- [Create a new branch on your
  fork](https://docs.github.com/en/get-started/quickstart/contributing-to-projects#creating-a-branch-to-work-on)
- [Make and push your changes to the forked
  repository](https://docs.github.com/en/get-started/quickstart/contributing-to-projects#making-and-pushing-changes)
- [Submit a pull request to the main
  repository](https://docs.github.com/en/get-started/quickstart/contributing-to-projects#making-a-pull-request)

Please make sure to include a clear and concise description of your changes in
your pull request.

### Commit Standards

This project uses the [Commitizen](http://commitizen.github.io/cz-cli) commit
standards to ensure consistent commit messages. If you're unfamiliar with all
the supported tags, it is recommended to use the [`git
cz`](https://github.com/commitizen/cz-cli) command, which will prompt you to
enter a commit message in the proper format.

### Tests

To preview a [GRUB](https://www.gnu.org/software/grub) theme without rebooting
your machine, consider using the
[`grub2-theme-preview`](https://github.com/hartwork/grub2-theme-preview)
utility.

### Modify the `theme.txt` file

All modifications to the `src/theme.txt` file should meet the requirements
specified in the [GRUB
documentation](https://www.gnu.org/software/grub/manual/grub/html_node/Theme-file-format.html).

### Add Icons

To add a new icon to the collection, follow these steps:

- Save the original high-resolution file in the `assets/icons` directory.
- Generate the icon in the `src/icons` directory.
- Ensure that the logo meets the requirements specified in the [GRUB
  documentation](https://www.gnu.org/software/grub). Specifically, ensure that
  the resolution of the icons is consistent with the others, and remove any
  unnecessary white space margins.

To remove unnecessary data from SVG files, consider using the
[`svgcleaner`](https://github.com/RazrFalcon/svgcleaner) utility.

To losslessy improve PNG compression, consider using the
[`oxipng`](https://github.com/shssoichiro/oxipng) utility. However, make sure to
include the `--ng` flag to prevent grayscale conversions, which seem
incompatible with [GRUB](https://www.gnu.org/software/grub).

### Add Fonts

To add a new font, follow these steps:

- Save the original font in a format such as OTF, TTF, or WOFF to the
  `assets/icons` directory.
- Generate a [GRUB supported](https://www.gnu.org/software/grub) font in the
  `src` directory with the [`grub-mkfont`](https://www.gnu.org/software/grub)
  utility.
- Include the new font in the `src/theme.txt` file.

## Code of Conduct

For information on the code of conduct for this project, please refer to
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## License

This project is licensed under [GNU GENERAL PUBLIC LICENSE Version
3](../LICENSE).
