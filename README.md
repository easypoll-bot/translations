# EasyPoll Translations
In this repository you can help us to translate EasyPoll into different languages.  
All translators who contribute high quality translations will be assigned the Translator role on our [Discord server](https://discord.gg/easypoll) to chat with other translators and staff members.

## How can I add a new language?
To add a new language, copy the English translation (`en-US.json`) and name the file according to the locale of Discord.  
It is important that the local is case-sensitive.  
In addition, only languages that are also available in Discord may be added.  

A list of all languages available on Discord can be found in the Discord documentation:  
https://discord.com/developers/docs/reference#locales


## How do I translate a language file?
The language files are structured in the Json format.  
To translate a file, edit the value of the translation strings (the blue part in the example).  
The key of the translation string (the green part in the example) is not allowed to be changed.

Example:
```json
"example_key": "Example value that needs to be translated!\nThis can contain {{variables}}, **formatting** and [links](https://easypoll.bot)."
```


## Formatting
Discord formatting in the translation strings such as `*`, `**`, `_`, `__` should be kept and not changed.  
Line breaks with `\n` should also be retained.  

Masked links (`[text](url)`) must also remain and only the text in the square brackets `[ ]` should be translated.  
It is important that the brackets `[ ]( )` remain together.  

Please read the Discord Text Formatting guide to learn more: [Markdown Text 101](https://support.discord.com/hc/en-us/articles/210298617-Markdown-Text-101-Chat-Formatting-Bold-Italic-Underline)


## Variables
Some translation strings contain variables such as `{{id}}` or `{{question}}` which are later automatically replaced by values such as the ID or question.  
The variables must be included in the translation and used sensibly. The part between the curly brackets `{{ }}` must not be translated or changed.

Example:
```json
"poll_id": "Poll ID: {{id}}"
```


## The meta section
There is a `meta` section at the top of every translation file. This contains important information about the translation.  
- `locale` must always match the Discord Locale
- `name` must always match the Discord Language Name
- `name_native` must always match the Discord Native Name
- `emoji_unicode` must match the correct flag of the locale and be specified as unicode.

Example:
```json
"meta": {
    "locale": "en-US",
    "name": "English, US",
    "name_native": "English, US",
    "emoji_unicode": "🇺🇸",
}
```

A list of all languages available on Discord can be found in the Discord documentation:  
https://discord.com/developers/docs/reference#locales


## How do I submit my translation?
You can submit your translations via a pull request in this repostiory.  
Please follow all instructions in this README file.  
Your translations and changes will then be checked by our team.


## Support
If you need technical help with translating, please contact us on our [Discord server](https://discord.gg/easypoll).


## Contributing Guidelines
- Translate strings without changing the context
- Variables must be preserved
- Text formatting must be preserved
- Do not add your own formatting to the texts _(E.g. write text bold that is not bold in the original translation)_
- Do not use any translator _(like Google Translate, DeepL, ...)_
- Do not change the file structure
- Only languages that are also [available in Discord](https://discord.com/developers/docs/reference#locales) may be added
- Only edit one language per pull request
