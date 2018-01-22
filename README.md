# Go SSH Tunnel package & tool

## Package

### Usage

```go
package main

import (
    sshTunnel "github.com/udondan/go-ssh-tunnel"
)

func main() {
    t := sshTunnel.New(8080, "example.com", 80)

    // do something with the tunnel

    t.Close()
    //give it a sec to close...
    time.Sleep(1 * time.Second)
}
```

## Tool

### Installation

```bash
go install github.com/udondan/go-ssh-tunnel/ssh-tunnel
```

### Usage 

```bash
ssh-tunnel --local 8080 --host example.com --remote 80
```

Press <kbd>Ctrl-C</kbd> to close the tunnel.