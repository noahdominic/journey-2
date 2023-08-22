# Journal-Rust

journal-rust is a simple command-line tool for maintaining a text-based journal.  This Rust project provides you with the ability to initialise your journal, create new entries, and open created entries.  Entries are stored as text files, which should make access and compatibility easy.

## Installation

In the future, you may download pre-compiled binaries in the Releases section.

### Building from source 

Make sure you have Rust and Cargo installed on your system.  You can install them by following the instructions on the [Rust website](https://www.rust-lang.org/tools/install).

Once Rust and Cargo are installed, you can clone this repository and build the `journal-rust` executable by running the following commands:

```bash
git clone https://github.com/your-username/journal-rust.git
cd journal-rust
cargo build --release
```

The compiled executable will be located at `target/release/journal-rust`.

## Usage

### Initializing the Journal

Before using the journal, you need to initialise it by running the `init` command.  This command sets up the necessary directory structure for storing your journal entries as well as stores information needed for generating new journal entry preambles.

```bash
journal-rust init
```

### Creating a New Journal Entry

To create a new journal entry, use the `new` command.  This command allows you to add a preamble for your entry, which will be written to today's entry file.  The tool will then open the text editor you set up during initialisation for you to complete the entry.

```bash
journal-rust new
```

For reference, here is an example of an entry's preamble:

```text
DATE: Tue, 2023 Aug 22 23:26:41 PST (+08:00)
LOCATION: University of the Philippines Cebu, Lahug, Cebu City

Temperature: 26 C, feels like 31.7 C, Overcast skies.
UV Index: 8.8  Sunrise: 05:35   Sunset: 17:59
Rain: 0 mm
Winds: 7.6 km/h SSW
Pressure: 1010.3 hPa
Humidity: 91%
Visibility: 11.32 km
```

### Opening Today's Journal Entry

To open today's journal entry, use the `open` command.  This allows you to add or modify the content of the entry. 

```bash
journal-rust open
```

### Getting Help

If you need assistance with the available commands, you can use the `help` command to display information about how to use the tool.

```bash
journal-rust help
```

or 

```bash
journal-rust -h
```

## Storage

Journal entries are stored as text files within the same directory as the config.toml that is created during the initialisation process.  Journal entries are stored within the directory structure in the format year/month/day.  For example, an entry for 14th March 2023, would be stored at ./2023/03/14.

## Licence

This project is licenced under the European Union Public Licence version 1.2 (EUPL-1.2). You can find the full text of the EUPL-1.2 licence in the [LICENCE](LICENCE) file.

---

Happy journaling!  If you have any questions or need further assistance, don't hesitate to reach out.