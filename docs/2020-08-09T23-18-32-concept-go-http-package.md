---
date: 2020-08-09T23:18:32-07:00
title: Concept-Go-Http-Package
tags: Go
---

# Concept-Go-Http-Package

Not providing specific IP on `http.ListenAndServe()` or `net.Listen()` means it can be reachable through all the IPs of the machine.

```go
package main

import (
	"fmt"
	"net/http"
)

type customerHandler struct{}

func (c customerHandler) ServeHTTP(w http.ResponseWriter, r *http.Request) {
	fmt.Println("path: ", r.URL.Path)
	fmt.Fprintf(w, "hello world")
}

func main() {
	var h customerHandler
	_ = http.ListenAndServe(":80800", h)
	/* 	if err != nil {
		log.Fatalf("error staring http server %v", err)
	} */
}
```

