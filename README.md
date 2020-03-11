# .doom.d

## System Prerequisites

### Global

Note: uses <https://github.com/lassik/emacs-format-all-the-code> under the hood
for code formatting.

```sh
yarn global add prettier
```

### Clojure

<https://github.com/hlissner/doom-emacs/tree/develop/modules/lang/clojure>

```sh
# Install clojure-lsp to local bin -- only do if (clojure +lsp)
# Note: +lsp is buggy: https://github.com/snoe/clojure-lsp/issues/81
wget https://github.com/snoe/clojure-lsp/releases/download/release-20200121T234305/clojure-lsp
chmod 755 clojure-lsp
mv clojure-lsp /usr/local/bin

brew install leiningen candid82/brew/joker
yarn global add node-cljfmt
```

### JavaScript/TypeScript

```sh
# NOTE: This is not really needed. Tide already is a emacs frontend for tsserver
yarn global add typescript-language-server # needed for (+lsp)
```

### Go

<https://github.com/hlissner/doom-emacs/tree/develop/modules/lang/go>

```sh
# NOTE: +lsp will use gopls
cd ~ # Run from root to install into GOPATH
go get -u github.com/motemen/gore/cmd/gore
go get -u github.com/stamblerre/gocode
go get -u golang.org/x/tools/cmd/godoc
go get -u golang.org/x/tools/cmd/goimports
go get -u golang.org/x/tools/cmd/gorename
go get -u golang.org/x/tools/cmd/guru
go get -u github.com/cweill/gotests/...
go get -u github.com/fatih/gomodifytags

brew install golangci/tap/golangci-lint
```

### Ruby

<https://github.com/hlissner/doom-emacs/blob/develop/modules/lang/ruby/packages.el>

```sh
gem install rubocop pry
```

### Markdown

<https://github.com/hlissner/doom-emacs/tree/develop/modules/lang/markdown>

```sh
yarn global add markdownlint textlint
brew install pandoc proselint
gem install mdl
```
