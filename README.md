# `go-monero`

### Daemon example:

```golang
daemon := monero.NewDaemonClient("http://127.0.0.1:18081/json_rpc", "rpcuser", "rpcpassword")
blockCount, err := daemon.GetBlockCount()
if err != nil {
  fmt.Println(err)
  return
} 
fmt.Println("Count:", blockCount)
```

### Wallet example:

```golang
wallet := monero.NewWalletClient("http://127.0.0.1:18082/json_rpc", "rpcuser", "rpcpassword")
balance, err := wallet.GetBalance()
if err != nil {
	fmt.Println(err)
	return
}
fmt.Println("balance:", balance)
```
