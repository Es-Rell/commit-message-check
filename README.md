# commit-message-check

一个简单验证commit提交规范，依赖于[husky](https://github.com/typicode/husky)

## 📦 Use

安装

```
npm i commit-message-check husky --save-dev
or
yarn add commit-message-check husky

yarn husky install
or
npm run husky install

npx husky add .husky/commit-msg ""  
```

In .husky/commit-msg 在文件末尾增加两行代码:

```
export GIT_PARAMS=$*
npx --no-install commit-check
```



## 🔨 Test

```
git add .
git commit -m"测试"
```

终端返回如下代表成功:

```
> git -c user.useConfigOnly=true commit --quiet --allow-empty-message --file -
   ERROR  提交日志不符合规范

  合法的提交日志格式如下(模块可选填):

    
        feat(模块): 添加了个很棒的功能
        fix(模块): 修复了一些 bug
        docs(模块): 更新了一下文档
        style(模块): 格式化代码结构（不影响代码运行的变动)
        UI(模块): 修改了一下样式
        chore(模块): 对脚手架做了些更改
        refactor(模块): 代码重构但不影响运行与功能

        其他提交类型: locale, perf, workflow, build, CI, typos, tests, types, wip, release, dep

husky - commit-msg hook exited with code 1 (error)
```


## 📝 Description
| type     | Description                                     |
| -------- | ----------------------------------------------- |
| feat     | 新功能（feature）                               |
| fix      | 修补bug                                         |
| docs     | 文档（documentation）                           |
| style    | 格式（不影响代码运行的变动）                    |
| refactor | 重构（即不是新增功能，也不是修改bug的代码变动） |
| tests    | 增加测试                                        |
| chore    | 构建过程或辅助工具的变动                        |
| perf     | 性能优化                                        |
| ...      | 更多暂不做解释😂                                 |



## 🔗 Link

- [更新日志](CHANGELOG.md)