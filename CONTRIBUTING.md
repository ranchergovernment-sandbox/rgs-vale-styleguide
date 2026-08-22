# Table of Contents  
- [Table of Contents](#table-of-contents)
- [Requesting Rule Changes](#requesting-rule-changes)
- [Contributing New Rules](#contributing-new-rules)
- [Requesting Hunspell Additions](#requesting-hunspell-additions)
- [Contributing Hunspell Additions](#contributing-hunspell-additions)


# Requesting Rule Changes  
When opening an issue requesting a rule change, explain clearly what the change request is. Is the request a change in `level`, an addition, or removal of a `token`, etc. If requesting a new rule ensure you explain why the new rule should exist. There are many valid reasons for a new rule, anywhere from ensuring grammatical correctness, to a style preference (this is a style linter after all).  

Certain rules are purely stylistic, there may be times where authors, and this repository disagree. In these cases, do keep in mind, individual rules can be disabled in the author's `vale.ini`.  

__Disable a Rule For The Entire Repository Example:__  
```ini
[*.md]
BasedOnStyles = RGS
RGS.ChicagoCapitalization = NO
``` 


# Contributing New Rules  
When contributing a Vale rule, you must ensure:  
1. Provide a document explaining the rule.
   1. A template can be found in: `./docs/templates/rule-explanation.md`.
   2. The template does not need to be followed perfectly, but the document must contain:  
      1. A link to the source rule in `./RGS/styles/RGS/`
      2. The level of the rule, i.e. suggestion, warning, error.
      3. The purpose of the rule.
2. The rule must link back to the document described above
   1. All Vale rules support a `link:` key, this must be a link back to the document in this repository.


# Requesting Hunspell Additions
The tech field is rife with uncommon words, and effectively has its own lexicon. As a result of this, it is permissible to request, or add jargon, and in some cases, slang.


# Contributing Hunspell Additions  
The files in `RGS/styles/config/dictionaries` are [Hunspell](https://hunspell.github.io/) files. Changes should be made to the correct dictionaries, there are no set rules, the rule of thumb though is:  
- en_US: Avoid editing. This is a standard dictionary and at any time could be overwritten with an updated upstream version. 
- SUSE: Only use for SUSE related words.
- RGS: This is the catch all. This is the default dictionary one should choose, unless there is a reason to use the others.
  

