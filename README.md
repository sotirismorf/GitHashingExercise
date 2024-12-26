# This repo is an exercise an Operating Systems course

This repo contains a script that takes in an input and generates a hash using
the sha256 algorithm.

This is the command that creates the hash. The `-n` argument on echo ensures
that no newline character is passed through stdin to `sha256sum`. The hash is
64 characters so we use head to output only the relevant characters of the
output.

```bash
echo -n "$INPUT" | sha256sum | head -c 64
```

Here's an example usage

```bash
./hash_script 1234 > hash_output.txt
```
