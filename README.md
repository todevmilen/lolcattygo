# LolcattyGo

LolcattyGo is a fun and colorful command-line utility that transforms piped text into rainbow-colored output, inspired by the popular `lolcat` tool. This project is written in Go and leverages RGB color cycling to make your terminal output visually engaging.

## Features

- Outputs text in a rainbow gradient.
- Reads input via pipes (e.g., `fortune | lolcattygo`).
- Written in Go, ensuring fast and efficient performance.

## Installation

1. Ensure you have Go installed on your machine. You can download and install Go from [golang.org](https://golang.org/dl/).
2. Clone this repository:
   ```sh
   git clone https://github.com/todevmilen/lolcattygo.git
   cd lolcattygo
   ```
3. Build the binary:
   ```sh
   go build lolcattygo
   ```
4. Move the binary to a directory in your `PATH` (optional):
   ```sh
   go install lolcattygo
   ```

## Usage

The tool is designed to be used with pipes in a terminal. For example:

```sh
fortune | lolcattygo
```

### Example

If you pipe the output of the `fortune` command:

```sh
fortune | lolcattygo
```

or

```sh
cat main.go | lolcattygo
```

You will see the output of `fortune` displayed in a rainbow gradient.

## How It Works

1. The program reads input from the standard input (stdin) using a `bufio.Reader`.
2. Each character is processed one at a time.
3. The RGB color values are calculated using sine functions to create a smooth gradient.
4. The colored character is printed to the terminal using ANSI escape codes.

## Limitations

- The tool is intended to be used with pipes and will display a message if no piped input is detected.
- It may not display colors correctly on terminals that do not support 24-bit (true color).

## Acknowledgments

- Inspired by the original `lolcat` tool.
- Written in Go for simplicity and performance.

---

Enjoy making your terminal more colorful with LolcattyGo! ✨
