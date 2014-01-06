# btcwallet

Simple command line bitcoin wallet

## Getting Started
Install the module with: `npm install btcwallet`

Set up your wallet with your bitcoin addresses and an encryption password:

```bash
$ btcwallet setup
Wallet location (~/.btcwallet.json): 
Password:
Private key (default: generate new): 

Created new wallet at ~/.btcwallet.json with initial address 17con3yx9Q4eEUvVXHTBkrZe8jtUU2bRXN.
Run `btcwallet add` to add more addresses.
```

Your wallet is stored in simple JSON, with each array item storing the public address and encrypted private address:

```javascript
{
  wallets: [
    ["17con3yx9Q4eEUvVXHTBkrZe8jtUU2bRXN", "lAroSwjSrzoukjz0sFK5iDR2fUQr7YXA9MsyhnXEs98pipnC15MHqJnslDaq7gTw46r8QB3rVKzX1u4ZgrflyLtf4ys5z41bpOfqDnhBhqRjdW92ot4U1RhFMQH5rHwloWGEyV8YTZUQ"],
    ["17con3yx9Q4eEUvVXHTBkrZe8jtUU2bRXN", "lAroSwjSrzoukjz0sFK5iDR2fUQr7YXA9MsyhnXEs98pipnC15MHqJnslDaq7gTw46r8QB3rVKzX1u4ZgrflyLtf4ys5z41bpOfqDnhBhqRjdW92ot4U1RhFMQH5rHwloWGEyV8YTZUQ"]
  ]
}
```

## Example use

Add more addresses:

```bash
$ btcwallet add
Password: 
Private key (default: generate new): 

Added new wallet with address: 17con3yx9Q4eEUvVXHTBkrZe8jtUU2bRXN
```

Check your balance:

```bash
$ btcwallet
1.042 BTC
```

Send money:

```bash
$ btcwallet send 0.01 17con3yx9Q4eEUvVXHTBkrZe8jtUU2bRXN
Password: 
Sent 0.01 BTC + 0.002 BTC to 17con3yx9Q4eEUvVXHTBkrZe8jtUU2bRXN
Balance: 1.02 BTC
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## License
Copyright (c) 2014 Christian Genco
Licensed under the MIT license.
