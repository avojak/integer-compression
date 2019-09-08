# integer-compression

Demonstrates several methods of integer compression:

- binary
- unary
- gamma
- delta

## Usage

### Compression

```
usage: compress [-h] M N

Compress an integer.

positional arguments:
  M           the compression method
  N           the integer to compress

optional arguments:
  -h, --help  show this help message and exit
```

For example:

```
$ ./compress gamma 3
101
$ ./compress gamma 5
11001
```

### Decompression

```
usage: decompress [-h] M C

Decompress an integer.

positional arguments:
  M           the compression method used
  C           the compressed integer to decompress

optional arguments:
  -h, --help  show this help message and exit
```

For example:

```
$ ./decompress gamma 101
3
$ ./decompress gamma 11001
5
```