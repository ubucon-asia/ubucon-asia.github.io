[![Deploy Website](https://github.com/ubucon-asia/ubucon-asia.github.io/workflows/Deploy%20Website/badge.svg)](https://github.com/ubucon-asia/ubucon-asia.github.io/actions?query=workflow%3A%22Deploy+Website%22)
# ubucon-asia.github.io
Website that contains index of Ubucon Asia events
Built with [Hugo](https://gohugo.io) and [Vanilla framework](https://vanillaframework.io/)

# Adding contents
You will need to install [Hugo CLI](https://gohugo.io/getting-started/installing/) to easily add contents.

To create new content, run the following command
```bash
# Create event content
hugo new --kind events events/<session-name>/_index.md
# Example: Create session content with title "Ubucon Asia 2021"
hugo new --kind events events/ubucon-asia-2021/_index.md
```

After that, You will find generated markdown file under `content` directory. Edit the markdown file to add details.
To add photo files, put files on content item directory.(The same path where content item's `_index.md` exists.)

# How to localize

1. Add language info in `config.yml` under `languages:` section. And fill out translation for site title, description and navigation menu. 
After adding language in `config.yml` you will be able to see your new language in language chooser menu.

```yml
languages:
  ko: # Language code
    languageName: 한국어 # Language name
    title: 우부콘 아시아
    weight: 2
    params:
      description: >- # description for event period
        2021년 부터 매년 Ubuntu 아시아 지역 커뮤니티를 모으고 연결하는 Ubuntu 컨퍼런스
    menu:
      main: # site navigation fields
        - identifier: events
          name: 행사 # Make sure to translate only "name" field
          url: events
          weight: 1
        - identifier: wiki
          name: 위키
          url: https://wiki.ubuntu.com/UbuconAsia
          weight: 5
```

2. UI localization  
You can see UI locale files in `i18n` directory. make a copy of `en.toml` And translate strings wraped with quotation marks. Below is an example.

```toml
[learn_more]
other = "Learn more"
```
```toml
[learn_more]
other = "더 알아보기"
```

3. Markdown content localization

Most markdown files are name `index.md` or `_index.md`. To translate, Make a copy of markdown file on same path. with the filename `index.<lang-code>.md` or `_index.<lang-code>.md` (e.g. `index.ko.md` or `_index.ko.md`). Then, translate the copied file.

Ubucon Asia 2021 website uses hugo's i18n feature to support localization. To learn more, please refer to ["Multilingual Mode"](https://gohugo.io/content-management/multilingual/)

# License
Code: MIT, Contents: CC BY 4.0
