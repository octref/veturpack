# Veturpack

A Vue project with minimal setup and dependencies for trying out [Vetur](https://github.com/vuejs/vetur)'s features. Also used for creating minimal, reproducible case for Vetur bug reports.

## Usage

- Install latest version of [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur)
- `git clone git@github.com:octref/veturpack.git`
- `cd veturpack`
- `yarn install`
- `code .`

## Things to Try

Try all features below in `src/Test.vue`. You can read more about these features in Vetur's documentation: https://vuejs.github.io/vetur/.

- Do an emmet expansion on the html template. For example, type `div` and then tab.
- Complete on `<router|`. Because of the [`vue-router`](https://router.vuejs.org/) dependency, you should see [`router-link`](https://router.vuejs.org/api/#router-link). Read more about this feature in [Framework Support](https://vuejs.github.io/vetur/framework.html).
- `yarn add element-ui`, reload the project and complete `<el`. You should see all tags from [Element UI](https://element.eleme.cn/#/en-US/component). Read more about this feature in [Framework Support](https://vuejs.github.io/vetur/framework.html).
- Complete on `<foo`. You should see `<foo-tag>`. Read more about this feature in [Framework Support](https://vuejs.github.io/vetur/framework.html).
- Hover over any tags such as `<div>` or `<router-link>`. You'll see the tag's description.
- Because of `"vetur.experimental.templateInterpolationService": true` in `.vscode/settings.json`, you should see an error on `{{ fo }}` in the template section. Change it to `foo` to fix the error.
- Delete the `foo` in {{ foo }}`. Type `b`. You should see completion of `bar`.
- In script section, try `_.`. You should see all [lodash](https://lodash.com)'s methods.
- Install another library with types, such as [jquery](https://api.jquery.com/). `yarn add -S jquery && yarn add -D @types/jquery`. After importing it with `import * as $ from 'jquery'`, you should get `$.` completions.
- Setup [eslint-plugin-vue](https://eslint.vuejs.org/user-guide/) with a `.eslintrc`. Set `"vetur.validation.template": false` to turn off Vetur's builtin ESLint linter. You'll get ESLint warnings now.
- In `<script>` section, add `//@ts-check`. Write some type-unsafe code, such as `let a = 'a'; a = 5`. You'll see an error.
- F1 -> Format the document. You can [configure](https://vuejs.github.io/vetur/formatting.html) the formatters and their settings as well.
- In `.prettierrc.json`, set `"singleQuote": true` and format again.
- Type `<style scss` and tab to choose a snippet. You should get a SCSS section setup. These snippets are [customizable](https://vuejs.github.io/vetur/snippet.html). 
- Try some CSS completions in the `<style lang="scss">` section.
- Make some errors in the Vue file and run [vti](https://vuejs.github.io/vetur/vti.html) — you should see all diagnostics printed on CLI.

## Next

For a more comprehensive setup, refer to https://github.com/chrisvfritz/vue-enterprise-boilerplate.

## License

MIT