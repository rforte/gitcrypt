This script is based on the idea of the node.js script cipherhub https://www.npmjs.com/package/cipherhub. I wanted an easy way to copy and paste passwords in slack without exposing (or logging) them in plain-text.

# Usage

## Encrypting some text.

```
echo "s3cr3tp@ssword" | ./gitcrypt -e rforte
```

## Decrypting some text.

```
./gitcrypt -d < secret.enc.txt
```

## Examples to make life easier. (mac osx)

```
echo "s3cr3tp@ssword" | ./gitcrypt -e rforte | pbcopy
```

Puts encrypted secret into your clipboard for easy pasting into slack/IM/iMessage etc.

Copy encrypted secret that someone sent you into your clipboard and run:
```
pbpaste | ./gitcrypt -d
```
