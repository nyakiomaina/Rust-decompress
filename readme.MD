# Rust Zip File Extractor
Rust Zip File Extractor is a simple Rust program that reads a zip file and extracts its contents, while maintaining the original directory structure.

## Usage
To use the Rust Zip File Extractor, you need to run the program with the name of the zip file as an argument. The zip file should be in the project's root directory.

Run the following command in the terminal:
```bash
cargo run your_file.zip
```
Replace ```your_file.zip``` with the name of your zip file. This will extract the zip file's contents into the current directory, replicating the directory structure of the zip file.

## How It Works
The application works as follows:

1. It checks the command-line arguments for the name of a zip file.
2. If the zip file exists, it opens the zip file and reads the contents.
3. It iterates over each item in the zip file.
4. If the item is a directory, it creates the directory in the current path.
5. If the item is a file, it creates the file in the current path.
6. It also sets the permissions for the files and directories (on Unix systems), matching the permissions set in the zip file.
7. Finally, it prints out information about each item it extracts, such as the item's index in the zip file, the path to which it was extracted, and its size (for files).