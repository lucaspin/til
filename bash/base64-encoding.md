Use the `base64` command to encode:

```bash
# Using normal stdout
echo "text-to-encode" | base64

# Using a file
base64 text-to-encode-file.txt

# To disable column wrapping
base64 -w 0 file.txt

# If you're on a Mac, the wrap option is called break
base64 -b 0 file.txt
```

And to decode:

```bash
# Using normal stdout
echo "text-to-decode" | base64 -d

# Using a file
base64 -d text-to-decode-file.txt

# If you're on a Mac, the decode option is with a capital D (WHY?)
echo "text-to-decode" | base64 -D
```