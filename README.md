# Chess-System-Tal-NNUE-2

Chess-System-Tal-NNUE-2 is a UCI chess engine written in C++ by Chris Whittington and Ed Schröder.

## Features

- UCI-compatible chess engine
- Approximately 50 Elo points stronger than our prior release Rebel 16
- Top five ranking among freely available chess engines

## Requirements

- User Interface (UI) software such as CuteChess, Banksia, or Arena

## Usage

1. Download and install a User Interface (UI) software compatible with UCI chess engines.
2. Load Chess-System-Tal-NNUE-2 as a chess engine in the chosen UI software.
3. Configure the opening book:
   - Ensure you have a folder containing the following polyglot book files: `polyglot-books/book.bin` and `polyglot-books/rebel.bin`.
   - To enable the book, use the UCI command: `setoption name Bookfile value book.bin` or `setoption name Bookfile value rebel.bin`.
   - Set the book depth using the command: `setoption name Bookdepth value N`, where N is a value between 0 and 200.
   - Adjust the random factor with: `setoption name Bookrandom value N`, where N is a value between 0 and 100.
4. Configure Learn Assist:
   - By utilizing an internal learned database, the engine search is weighted to prefer certain lines.
   - To turn off Learn Assist, use the command: `setoption name Favouredmovedepth value 0`.
   - To enable Favoured Move, use: `setoption name Favouredmovedepth value N`, where N is a value between 1 and 100.
   - Adjust the random factor with: `setoption name Favouredmoverandomiser value N`, where N is a value between 0 and 100.

## Contributing

Contributions to Chess-System-Tal-NNUE-2 are welcome! If you would like to contribute, please contact us at https://prodeo.actieforum.com/

