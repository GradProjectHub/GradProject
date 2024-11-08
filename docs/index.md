# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

起動コマンドは [mkdocs serveコマンドオプション](https://fig.io/manual/mkdocs/serve)

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

```go title="main.go"
# Code block content
package main

import (
	"fmt"
	"time"
)

func main() {
	fmt.Println(time.Now())
}
```