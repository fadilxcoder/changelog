# Notes

- [keep a changelog](https://keepachangelog.com/en/1.0.0/)
- [Conventional Changelog Configuration Spec (v2.1.0)](https://github.com/conventional-changelog/conventional-changelog-config-spec/blob/master/versions/2.2.0/README.md)
- [Examples](https://www.conventionalcommits.org/en/v1.0.0/#examples)
- [GIT auto-changelog](https://github.com/CookPete/auto-changelog)
- Example of generated changelog locally - [CHANGELOG.md](https://github.com/ifx-code/changelog/blob/4f15e65511a19bed7ed675c70433e8cd2972fe02/CHANGELOG.md)
- Add `.auto-changelog`

```
...
Usage: auto-changelog [options]

Options:

  -o, --output [file]                 # output file, default: CHANGELOG.md
  -c, --config [file]                 # config file location, default: .auto-changelog
  -t, --template [template]           # specify template to use [compact, keepachangelog, json], default: compact
  -r, --remote [remote]               # specify git remote to use for links, default: origin
  -p, --package                       # use version from package.json as latest release
  -v, --latest-version [version]      # use specified version as latest release
  -u, --unreleased                    # include section for unreleased changes
  -l, --commit-limit [count]          # number of commits to display per release, default: 3
  -b, --backfill-limit [count]        # number of commits to backfill empty releases with, default: 3
...

```

- Install `npm i auto-changelog`
- Add to `package.json`
- RUN 
- - `npm run changelog`
- - `./node_modules/.bin/auto-changelog --latest-version 0.1.0`
- - `npm run changelog 0.1.1`