[![codecov](https://codecov.io/gh/gofika/regexputil/branch/main/graph/badge.svg)](https://codecov.io/gh/gofika/regexputil)
[![Build Status](https://github.com/gofika/regexputil/workflows/build/badge.svg)](https://github.com/gofika/regexputil)
[![go.dev](https://img.shields.io/badge/go.dev-reference-007d9c?logo=go&logoColor=white)](https://pkg.go.dev/github.com/gofika/regexputil)
[![Go Report Card](https://goreportcard.com/badge/github.com/gofika/regexputil)](https://goreportcard.com/report/github.com/gofika/regexputil)
[![Licenses](https://img.shields.io/github/license/gofika/regexputil)](LICENSE)

# regexputil

golang regexp utils for common use


## Basic Usage

### Installation

To get the package, execute:

```bash
go get github.com/gofika/regexputil
```

### Example

```go
package main

import (
	"fmt"

	"github.com/gofika/regexputil"
)

func main() {
	bar, matched := regexputil.Match(`Foo(.+)`, "Foobar") // bar="bar" matched=True
	fmt.Printf("bar: %smatched: %v\n", bar, matched)

	matched = regexputil.IsMatch(`Foo(.+)`, "Foobar") // matched=True
	fmt.Printf("matched: %v\n", matched)
}
```