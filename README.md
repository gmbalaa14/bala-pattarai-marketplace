# Bala Pattarai Marketplace

Plugin marketplace for **Bala's Pattarai**: hand-forged developer skills for Claude Code.

This repository holds only the marketplace catalog. The skills themselves live in the plugin repository, so installing from here pulls just the plugin and nothing else.

## Install (Claude Code)

```
/plugin marketplace add gmbalaa14/bala-pattarai-marketplace
/plugin install thiran@bala-pattarai
```

## Plugins

| Plugin | Description | Source |
|---|---|---|
| `thiran` | Developer workflow skills: plan features, write conventional commits, rebase safely, and triage and judge PR review comments. | [`plugins/thiran`](https://github.com/gmbalaa14/thiran-pattarai/tree/main/plugins/thiran) |

Skills in `thiran`: [`plan-with-me`](https://github.com/gmbalaa14/thiran-pattarai/tree/main/plugins/thiran/skills/plan-with-me), [`commit-msg`](https://github.com/gmbalaa14/thiran-pattarai/tree/main/plugins/thiran/skills/commit-msg), [`safe-rebase`](https://github.com/gmbalaa14/thiran-pattarai/tree/main/plugins/thiran/skills/safe-rebase), [`pr-triage`](https://github.com/gmbalaa14/thiran-pattarai/tree/main/plugins/thiran/skills/pr-triage), [`pr-judge`](https://github.com/gmbalaa14/thiran-pattarai/tree/main/plugins/thiran/skills/pr-judge).

## Links

- **Skills and plugin source:** [gmbalaa14/thiran-pattarai](https://github.com/gmbalaa14/thiran-pattarai). Report issues and contribute here.
- **Documentation:** [gmbalaa14.github.io/thiran-pattarai](https://gmbalaa14.github.io/thiran-pattarai/)

## How it works

`.claude-plugin/marketplace.json` lists each plugin with a `git-subdir` source that points at the plugin repository. Claude Code fetches only `plugins/thiran` from it. Plugin versions come from the plugin's own `plugin.json`, so there is nothing to bump here on release.

## Migrating from the old marketplace

If you installed `thiran@pattarai` from `gmbalaa14/thiran-pattarai`, switch to this marketplace:

```
/plugin uninstall thiran@pattarai
/plugin marketplace remove pattarai
/plugin marketplace add gmbalaa14/bala-pattarai-marketplace
/plugin install thiran@bala-pattarai
```

Do not enable both at once, or the skills will load twice.

## License

[MIT](LICENSE) © 2026 Balagurunathan Marimuthu
