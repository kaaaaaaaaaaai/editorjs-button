![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Set Link and Text and Generate button plugin for Editor.js

![画面収録 2020-12-13 16 59 53](https://user-images.githubusercontent.com/2194021/102006852-7a6fb880-3d67-11eb-98d2-20b7e88672df.gif)

## Installation

### Install via NPM

Get the package

```shell
npm i --save editorjs-button
```

Include module at your application

```javascript
const anyButton = require('anyButton');
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN

`https://cdn.jsdelivr.net/npm/editorjs-button@1.0.0`

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
tools: {
        AnyButton: {
          class: AnyButton,
          inlineToolbar: false,
          config:{
            css:{
              "btnColor": "btn--gray",
            }
          }
        },
      },
      i18n: {
        messages: {
          tools: {
            "AnyButton": {
              'Button Text': 'ボタンに表示するテキスト',
              'Link Url': 'ボタンの飛び先のURL',
              'Set': "設定する",
              'Default Button': "デフォルト",
            }
          }
        },
      },
}
```

## Config Params

`i18n` overwrite if want to change default placeholder text,

```
i18n: {
    messages: {
      tools: {s
        "AnyButton": {
          'Button Text': 'ボタンに表示するテキスト',
          'Link Url': 'ボタンの飛び先のURL',
          'Set': "設定する",
          'Default Button': "デフォルト",
        }
      }
    },
},
```

if customize css, input filed, button design, and etc... 

```
config:{
    css:{
      "btnColor": "btn--gray",
    }
}
```

## Output data

| Field  | Type     | Description      |
| ------ | -------- | ---------------- |
| link   | `string` | Exclusion HTML Tag text |
| text   | `string` | Exclusion HTML Tag text |


```json
{
            "type" : "AnyButton",
            "data" : {
                "link" : "https://editorjs.io/",
                "text" : "editorjs official"
            }
        }
```

