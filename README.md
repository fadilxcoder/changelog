# Notes

- [How to Automatically Generate Changelog for your node.js projects](https://dev.to/brayanarrieta/how-to-automatically-generate-changelog-for-your-node-js-projects-43jk)
- [Conventional Changelog Configuration Spec (v2.1.0)](https://github.com/conventional-changelog/conventional-changelog-config-spec/blob/master/versions/2.2.0/README.md)
- [Examples](https://www.conventionalcommits.org/en/v1.0.0/#examples)
- Add `.versionrc.json`

```
{
    "types": [
        {"type": "feat", "section": "Features"},
        {"type": "fix", "section": "Bug Fixes"},
        {"type": "chore", "hidden": true},
        {"type": "docs", "hidden": true},
        {"type": "style", "hidden": true},
        {"type": "refactor", "hidden": true},
        {"type": "perf", "hidden": true},
        {"type": "test", "hidden": true}
    ],
    "commitUrlFormat": "https://github.com/ifx-code/changelog/commits{{hash}}",
    "compareUrlFormat": "https://github.com/ifx-code/changelog/compare/{{previousTag}}...{{currentTag}}"
}
```

- Install `npm install --save-dev standard-version`
- Add to `package.json`

```
"scripts": {
...
    "release": "standard-version",
    "release:minor": "standard-version --release-as minor",
    "release:patch": "standard-version --release-as patch",
    "release:major": "standard-version --release-as major"
...
```

- Git commands : 
- - `git add ....`
- - `git commit`
- - Based on current configs, commit message will be :

```
feat(app): Initialize project

Setting up project structure

Repo structure - dependencies, classes, modules, apps, node_modules

Reviewed-by: ABX
Refs: #123
```

```
fix(app): Updating readme

Updating readme documentation
```