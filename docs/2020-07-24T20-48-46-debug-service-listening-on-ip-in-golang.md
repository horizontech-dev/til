---
date: 2020-07-24T20:48:46-07:00
title: Debug-Service-Listening-On-Ip-In-Golang
tags: networking
---

# Debug-Service-Listening-On-Ip-In-Golang

```go
package main

import (
    // "fmt"
    // "io"
    "net/http"
    "log"
)

func HelloServer(w http.ResponseWriter, req *http.Request) {
    w.Header().Set("Content-Type", "text/plain")
    w.Write([]byte("This is an example server.\n"))
    // fmt.Fprintf(w, "This is an example server.\n")
    // io.WriteString(w, "This is an example server.\n")
}

func main() {
    http.HandleFunc("/hello", HelloServer)
    err := http.ListenAndServeTLS(":443", "server.crt", "server.key", nil)
    if err != nil {
        log.Fatal("ListenAndServe: ", err)
    }
}
```

The above code will listen on ipv6. 

If you want your service to listen on ipv4, then you can achieve that using **net** package

```go
	// Making the server to listen on tcp4
	// https://github.com/golang/go/issues/5197
	l, err := net.Listen("tcp4", ":443")
	if err != nil {
		log.Fatal(err)
	}				
```

