# cowsay in Brainfuck

This is a simplified implementation of cowsay written in Brainfuck.

## Examples

### Default cow

    echo "Hello, I'm a cow" | bf cowsay.bf


```
 __________________
< Hello, I'm a cow >
 ------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

### Paranoid cow

If your sentence ends with an exclamation mark the behavior is equivalent to the `-p` option of the original cowsay program.

    echo "MOO!" | bf cowsay.bf

```
 ______
< MOO! >
 ------
        \   ^__^
         \  (@@)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

### Dead cow

Unfortunately, this program doesn't support multiline messages. To compensate for this missing feature, I implemented an enhanced version of the dead cow. You can kill the cow providing an empty input.

    echo "" | bf cowsay.bf

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@ Empty input provided. Cow crashed @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

              ||     ||
              ||----M |
          (--)/       )/\/
          (xx)/-------
          v--v
```