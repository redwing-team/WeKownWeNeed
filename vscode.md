# vscode

* [官网][1]

## 配置

推荐在项目中使用 `.vscode/setting.json` 文件保存配置。推荐配置如下：

``` json
{
    "javascript.validate.enable": false,
    "editor.wrappingColumn": 100,
    "files.eol": "\n",
    "beautify.onSave": ["js", "css", "html"],
    "beautify.language": {
        "css": [
            "less"
        ],
        "html": [
            "vue"
        ]
    },
    "beautify.onSaveIgnore": [
        "**/node_modules/**",
        "**/*+(.|_|-)min.*"
    ]
}

```

## 插件

* [beautify][2]

    它是一款javascript, JSON, CSS, 和HTML代码格式美化工具，在 [js-beautify][3] 的基础上实现的。

    推荐在项目中使用 `.jsbeautifyrc` 文件保存配置。推荐配置如下：

    ``` json
    {
        "eol": "\n",
        "e4x": true,
        "js": {
            "end_with_newline": true
        },
        "html": {
            "extra_liners": []
        }
    }
    ```

* [ESLint][4]

    由微软官方维护的一款整合进 VSCode 的 [ESlint][5] 插件。

    推荐在项目中使用 `.eslintrc` 文件保存配置。推荐配置如下：

    ``` json
    {
        "env": {
            "browser": true,
            "es6": true,
            "node": true
        },
        "parser": "babel-eslint",
        "extends": "airbnb-base",
        "plugins": [
            "html"
        ],
        "parserOptions": {
            "ecmaVersion": 6,
            "ecmaFeatures": {
                "experimentalObjectRestSpread": true,
                "jsx": true
            },
            "sourceType": "module"
        },
        "rules": {
            "comma-dangle": [2, "never"],
            "no-console": 0,
            "no-alert": 0,
            "indent": [2, 4, {
                "SwitchCase": 1
            }]
        }
    }
    ```

    > 特别注意，VSCode 当前版本（1.6.1）不支持对 `<script>` 标签内的 `JS` 代码进行验证，[issue][6]。

* [stylelint][7]

    > A mighty, modern CSS linter that helps you enforce consistent conventions and avoid errors in your stylesheets.

    推荐在项目中使用 `.stylelintrc` 文件保存配置。推荐配置还在整理中：

    ``` json
    ```

## 参考

* [`script` 标签里的 js 代码没提示](https://www.zhihu.com/question/43918020)
* [vscode 的界面是用的什么技术？](https://www.zhihu.com/question/43666493)

[1]:http://code.visualstudio.com
[2]:https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify
[3]:https://github.com/beautify-web/js-beautify
[4]:https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
[5]:http://eslint.org/
[6]:https://github.com/Microsoft/vscode-eslint/issues/21
[7]:https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint