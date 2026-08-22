# Table of Contents
- [Table of Contents](#table-of-contents)
- [RGS Vale Style Guide](#rgs-vale-style-guide)
  - [Rules](#rules)
- [How To Use This Repository](#how-to-use-this-repository)
  - [Sample Configuration](#sample-configuration)


# RGS Vale Style Guide
This repository is a Vale compatible style package based off of SUSE's own package. This repository can be consumed by any author via Vale to ensure consistency in tone, and style while also providing a simple spell check. 


## Rules  
All rules are documented in the `docs/rules` directory, each rule has a severity level (suggestion, warning, or error), and purpose:  
- [ChicagoCapitalization](./docs/rules/ChicagoCapitalization.md)
- [Contractions](./docs/rules/Contractions.md)
- [CorporateSpeak](./docs/rules/CorporateSpeak.md)
- [DoubleDash](./docs/rules/DoubleDash.md)
- [Editorializing](./docs/rules/Editorializing.md)
- [Link](./docs/rules/Link.md)
- [Quotes](./docs/rules/Quotes.md)
- [Repetition](./docs/rules/Repetition.md)
- [RGS-Products](./docs/rules/RGS-Products.md)
- [Semicolons](./docs/rules/Semicolons.md)
- [Spacing](./docs/rules/Spacing.md)
- [Spelling](./docs/rules/Spelling.md)
- [SUSE-Products](./docs/rules/SUSE-Products.md)
- [Terms-IgnoreCase](./docs/rules/Terms-IgnoreCase.md)
- [Terms](./docs/rules/Terms.md)
- [Usage](./docs/rules/Usage.md)
- [Will](./docs/rules/Will.md)
- [Wordiness](./docs/rules/Wordiness.md)


# How To Use This Repository  
1. Follow the [Vale installation docs](https://docs.vale.sh/topics/installation).
2. Consume this package by placing a configuration file at the top level directory. 
3. Run `vale sync` to pull the RGS package down.


## Sample Configuration  
This is a minimal Vale configuration file (`.vale.ini`). This should be in the top level directory in your repository.
```ini
# This places the style in a .github/vale local directory. 
# This is not needed, but does keep vale info in a hidden directory.
StylesPath = ./.github/vale
# This downloads the RGS style zip, this needs to come from a release, it can not come from a branch.
Packages = https://github.com/ranchergovernment-sandbox/rgs-vale-styleguide/releases/download/v0.1.0/RGS.zip

# Apply x configs to any .md file
[*.md]
# Apply the RGS style (this repository)
BasedOnStyles = RGS
```

> [!NOTE]  
> You should add the RGS vale files to your .gitignore. If you are using the above example, the following should work:  
> ```
> .github/vale/RGS
> .github/vale/config/dictionaries
> ```