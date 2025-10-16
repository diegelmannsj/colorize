# 🎨 Colorize

A versatile Bash script to print text in true color (24-bit) directly in your terminal, specified by HEX or RGB values. Includes options for generating color shades and complementary colors.

## Installation

1.  Make the script executable:
    ```bash
    chmod +x colorize
    ```
2.  Move it to a directory in your PATH:
    ```bash
    sudo mv colorize /usr/local/bin/
    ```

## Usage

```
colorize [options] [<text...>] <color>
```

### Options (case-insensitive)
* `-s`, `--shades`: Display the color, plus 5 darker and 5 lighter shades.
* `-c`, `--complementary`: Display the complementary color.
* `-cs`, `-sc`: Enable both shades and complementary modes.
* `-t`, `--text <string>`: Specify the text to color. Overrides positional text.

### Examples

**Basic Usage**
```bash
# Using a HEX color
colorize 'Hello, World!' '#4285F4'

# Using an RGB color
colorize 'This is red.' '255,0,0'
```

**Generate Shades**
```bash
# Get 11 shades of a color using the default text
colorize -s ff7f50
```

**Show Complementary Color**
```bash
colorize --complementary 'Base and Complement' '008080'
```

**Combine Shades & Complementary**
```bash
colorize -cs 'All the colors!' 4B0082
```

**Specify Text with a Flag**
```bash
colorize -s --text "My text here" C51077
```
