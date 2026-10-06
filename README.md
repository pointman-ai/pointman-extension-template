# hello: a Pointman extension template

One command, `hello.greet`, that writes a greeting to a file and reports it. Make a repo from this
template (https://github.com/pointman-ai/pointman-template) named `pointman-<id>`, with the topic
`pointman-extension`. Rename `hello` everywhere (the id in extension.toml, the folder, and the command,
tool and event names), and write your own commands in `hello/__main__.py`. It's MIT, as every
extension repo is by default.

- **Run the tests:** `uv run pytest`. They start the extension the way a node does, against a
  stand-in node from `pointman-extension`, which also answers secrets within the manifest's
  permissions.
- **Try it on a machine:** `pointman add <this repo's folder>`, for development, then run its
  command from any thread. Once it has a release, `pointman add hello` brings it into the workspace's
  catalogue (an owner) and installs it, and `pointman upgrade` moves machines to newer releases.
- **The protocol and the manifest:** docs/dev/extensions.md in Pointman's repo.
