# Chess-System-Tal-NNUE-2
UCI Chess engine written in C++ by Chris Whittington and Ed Schröder

CSTal is a UCI engine and needs a User Interface (UI) such as CuteChess, Banksia or Arena to run.

CSTal is the big brother of Rebel 16, and is about 50 Elo pts stronger, putting it in at least the top five of freely available chess engines.

Opening Book: 
Assuming you have a folder containing these two polyglot book files:
polyglot-books/book.bin and polyglot-books/rebel.bin, 
Turn book On: UCI command "setoption name Bookfile value book.bin" or "setoption name Bookfile value rebel.bin"
Set Book Depth: "setoption name Bookdepth value N" where N is 0-200
Set Random factor "setoption name Bookrandom value N" where N is 0-100

Learn Assist:
Using an internal learnt database, the engine search is weighted to prefer certain lines
Turn Learn Assist Off: "setoption name Favouredmovedepth value 0"
Turn Favoured Move On: "setoption name Favouredmovedepth value N" where N is 1-100
Set Random factor "setoption name Favouredmoverandomiser value N" where N is 0-100

