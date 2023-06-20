# Chess-System-Tal-NNUE-2

Chess-System-Tal-NNUE-2 is a UCI chess engine written in C++ by Chris Whittington and Ed Schröder.

## Features

- UCI-compatible chess engine
- Specifically designed to play in style of the legendary Tal
- Public executable, private source code
- Elo 2914 Blitz rating on Nightmare.nl server
- June Blitz 2023 authors tourney, 1st=
- Previous Blitz tourney 2nd=
- Previous Blitz tourney outright 1st
- Top five ranking (probably) among freely available chess engines

## Requirements
- AVX2 compatible PC
- User Interface (UI) software such as CuteChess, Banksia, or Arena

## Usage

1. Download and install a User Interface (UI) software compatible with UCI chess engines.
2. Load Chess-System-Tal-NNUE-2 as a chess engine in the chosen UI software.
3. Hash, Threads, Ponder
   - setoption name Hash value N to set Hash table size
   - setoption name Threads value N to set Threads (limited to max(1, cores/2), some UI programs and Windows can't cope with high core count)
   - setoption name Ponder value N to turn Pondering on or off
5. Configure the opening book:
   - Ensure you have a folder containing the following polyglot book files: `polyglot-books/book.bin` and `polyglot-books/rebel.bin`.
   - To enable the book, use the UCI command: `setoption name Bookfile value book.bin` or `setoption name Bookfile value rebel.bin`.
   - Set the book depth using the command: `setoption name Bookdepth value N`, where N is a value between 0 and 200.
   - Adjust the random factor with: `setoption name Bookrandom value N`, where N is a value between 0 and 100.
6. Configure Learn Assist:
   - By utilizing an internal learned database, the engine search is weighted to prefer certain lines.
   - To turn off Learn Assist, use the command: `setoption name Favouredmovedepth value 0`.
   - To enable Favoured Move, use: `setoption name Favouredmovedepth value N`, where N is a value between 1 and 100.
   - Adjust the random factor with: `setoption name Favouredmoverandomiser value N`, where N is a value between 0 and 100.
7. For Power Users
   - Windows and some UI's can become unstable if threads are set too high, use at your own risk
   - setoption name RelaxThreadLimit value N (set yourself as a power user)
   - setoption name LoadNNUE value (save and load NNUE files)
   - setoption name SaveNNUE value 

## Contributing

Contributions to Chess-System-Tal-NNUE-2 are welcome! If you would like to contribute, please contact us at https://prodeo.actieforum.com/

## Reviews of the Old Chess System Tal, published by Chris Whittington, from the end of the last century
"The Chess System Tal programs were created by Chris Whittington in the 1990's and marketed by his company, Oxford Softworks. Their creation was guided by Whittington's philosophy that encoding knowledge into a chess program is much preferable over fast and deep searches.
CSTal is designed to play in the romantic and dangerous style of Michael Tal, famous for his daring and aggressive style of play."

"Programmer Chris Whittington has developed a radically different approach to chess programming, concentrating on speculative chess knowledge within the evaluation function; and the use of forward pruning techniques which rely on this evaluation function knowledge."

"One effect of using a high knowledge-based approach is that CSTal operates at a nodes per second rate much less than programs with simple evaluation functions. The risks and benefits of this strategy are obvious; on the one side CSTal is able to steer games towards tactical king-attack complexities, and to execute stunning sacrifices. On the other side the disparity in effective search depth means that state of the art search programs will have the advantage if the position does not contain factors where CSTal's knowledge is able to give it the edge."

"CSTal's computer-computer games are often very exciting and double-edged, with the result in doubt until the end. It is capable of causing serious upsets to top programs, but also of being seriously upset itself."

2In a materialistic world, in the materialistic world of computer chess, Chess System Tal offers the alternative pathway of idealism.
Chris Whittington's philosophy of knowledge over search can be best described by his own words:

It's the search gap. Gettit ? Out of this search gap comes all the naive speculation and nonsense that gets written. The program has every style and no style, it has no consistency to play against, only materialism, you can't learn from it, tomorrow it will be different (found another mine in the search gap), only the difference is just a relection of - whoops, trod on another mine. What can you do with such a program ? Use the take-back key and try again ? - and imagine this helps you improve or learn ?

Now, I claim this search gap has no meaning or understanding possibilities for a human. That a human can't relate his heuristics to it. That you can't extract the knowledge out of it and represent it to a human. That you can't even extract the knowledge out of it and represent it to yourself. You can't get heuristics from it. So I call it counting beans - useless for us humans.

Now, take a knowledge program, you can play it and see the play style. You can try and work out what it does and why. There'll be a reason, based on human chess heuristics. The game has plan, and flow, and doesn't consist of hidden minefields. It won't grind you down by search, it will try speculative ideas which it might, or might not, be able to get to work. You can see the speculative ideas, and try them yourself. I think you can, as a human, relate to this type of program. If you know the programmer, maybe you can see patterns into the program that come from him, and so on. I think these types of programs are infused with some force, in so far as any chunk of silicon can be."

"Chess System Tal contained some of the essence of this philosophy. By all accounts its sequel, Chess System Tal 2 (written for Windows), was this philosophy captured in code. By all accounts, CSTal 2 was a masterpiece as a chess program for humans to play against. Aggressive, speculative, unsound. But, above all, the chess it played was exciting and interesting."
"Just curious. We saw human player make unsound sac[rifice] all the time, at least in club level. That often leads to a more exciting and interesting game or more humanly game. We, human, saw the opportunity, but don't know the outcome within our calculating power, we gamble! Sometime we win sometime lose.
"Chess softwares, which been lowed their strenth to club level, seem not doing so. They reduce their playing strenth by hanging pieces or reduce searching time. This make playing against them rather dull.
"May be this is a desired feature of some top comercial software."
Yibing Fan, December 1, 1999
"...CST-2 makes unsound sacrifices and also makes some brilliant sacrifices. That is what makes playing it so much fun. You never know when one of those things are coming! The unsound ones help to lower the rating and I'm not sure if there are enough sound sacs to make up for them but it makes for a lot of fun and can be un-nerving. You may find yourself losing to an unsound sac if you are not careful."
Jim Walker, December 1, 1999

"Chess System Tal [2] makes great [sacrifices].
"It's something of a challenge to make them play credible ones, but it's fairly easy to make them play stupid ones.
"For instance, if you start adding opposite castling king terms, you'll start sacrificing your h-pawn even when it makes no sense, for instance when there are no rooks on the board.
" I still think that CST[2]'s are the most creative. Some of the games Thorsten has posted have featured sacrifices that are creative even by human standards, in my opinion. Most computer sacrifices seem very wooden compared to these."
Bruce Moreland, December 1, 1999

"I agree. I once saw what COULD be considered a standard sac on h3 from Black's point of view, except that I couldn't see how CST[2] was going to follow up as its pieces didn't seem properly poised to do so. 10-15 moves later, it came through. Very impressive."
Albert Silver, December 2, 1999

"Which of these programs is stronger at the tournament level - CSTal 2 or Chess Partner 4.1? Are there any features that may make one of the programs unique compared to the other?"
O.Veli, May 20, 1999

"WCSTAL[2] is a lot stronger by far and a lot, lot prettier. No comparison possible."
Fernando Villegas, May 12, 1999
"Another feature you might like: you can use CSTAL[2] as an Interface for playing on chess servers if you are bored to play only with your friend on LAN. At tournament time control TAL belongs to the absolute top group of the chessprogs by the way."
Pete, May 12, 1999

"I have the feeling, almost the certitude, that the key of the difference [from other programs] is that CSTAL[2] does not use the usual maxmin approach, that is to say, does not choose a move because even the best of the possible answers - for the opponents - has less score than the best of the answers of other moves. I believe that some kind of preference is given to moves where there are the maximal number of dangerous answers from the opponent FOR the opponent. In other words, CSTAL[2] does not presumes the best possible answer from the opponents, BUT prefer to give the opponent the greatest number of wrong moves to choose from, even if there is a good move that is better than any other."
Fernando Villegas, May 12, 1999

"[A]n intelligent chess program will give you opportunity to train manouvres, plan and [strategy] skills and tactical skills too.
"So this is a list of the best chess programs (in my own opinion) that could meet the requirements for training: (the order is alphabetical order)
Chess System Tal (Win or DOS version)
Hiarcs 7 (or even Hiarcs 6)
Rebel 10"
Ricardo Sant'Ana, May 9, 1999

"CSTal [2] plays on ICC very successful til now! No lost or remis game against any human, and a very nice win against Crafty 16.6 (about 2800) with a long term speculative sacrifice! The only lost game was one against Fritz 5 (lost on time in a technically drawn position!).
"CSTal [2] crushed some strong humans who wanted to apply an anti-computer strategy. Often it does not win it's games but destroys the other players. Actual ICC blitz rating is 2539 at a 200 MHz MMX, but it is increasing with almost every game I play!"
F.Jermann, May 8, 1999

"I'm doing all I can to popularize [CSTal-2] among strong players (which is why I'm playing the faster, more popular time controls). I've noticed that if I take the time to properly explain what the program is about, many of them do get curious about playing it. If more would be willing to take it on, I can see it approach the 3000 plateau, even in fast blitz, which is not its forte!...
"GM Agokoy (Eugene Torre's anonymous handle ....shhhh :-) really enjoys playing it-- he was even unsure if it was a computer after all !! IM Ceres (anon) was also impressed"
Shyborg, April 28, 1999

"This program (CSTal-2) is fun to play...
"This sure looks like the meanest program against humans. One of the very few programs to be developed by a master, it DOES play like Tal --it's no joke!!
"... So if you need convincing, try it. It won't wait for you to blunder, it'll just outplay you from the start!"
Shyborg, April, 1999

"Shyborg (C), running CSTAL2-Win, has maintained a near 2800 blitz rating on icc, playing only blitz games (time=<5), and mainly against somewhat lower rated human opponents. It seems very tough to play against on a p2-400. If more GMs were willing to play it, I suspect it could even go higher."
Greg Moller, April 20, 1999

"It is my particular black beast. For a reason or another thet bloody program...gets me all the [time], no way. I can defeat genius but I cannot defeat Tal ."
Fernando Villegas, March 30, 1999

"In contrast to almost all other chess software authors, Chris Whittington chooses a different way. He implements a lot of chess knowledge into his program because he does not like brute force methods. So CSTal often produces excellent games. On the other hand there are also blunders sometimes! But because of this approach a lot of customers are interested in this program."
Gambit-Soft, March 30, 1999

"Just play a "nothing" position, one with no tactics, maybe partially blocked, against a fast-searcher.
"What will it teach you? Or better yet, what will it NOT teach you? I think a computer should be best judged on how it succeeds in formulating plans, and most of this stuff occurs in these "nothing" positions. Forget about hard-to-fathom deep "truths". No such thing-- plus, you'll never get to use such "results", (except maybe in some rare opening bust). If you or I solved chess today, neither one of us could live long enough to show it to anyone...
"Flashy, unfathomable tactics have limited value to the average player. Plans are much more important. One outstanding program that_attempts_to "plan" while still playing dazzling enough tactics is CSTal. And, unlike the fast-searchers, you won't have to blunder against it to lose-- even if you keep the position relatively free of tactics, it will still come after you (with energetic play and sacs even), just as if you played against a strong human player!"
Anon on Chess News Group, March 09, 1999

"I appreciate the direction you are taking with CST. I enjoy the wild sacrificial style, which is not always correct, but it is amazing how *close* to correct it seems to be. The attacks I have seen seem to have substance, and they do appear out of nowhere.
"I think it is likely that your program entertains its customers much more than other programs do, and it probably also teaches them things they can't learn from other programs.
"I don't know whether or not your approach will ever result in a score in excess of 50% against everything else on even hardware, but if I were in your shoes I wouldn't care that much, I would keep optimizing for insanity and hoping that potential customers could take their eyes off the Swedish list long enough to contemplate issues of style."
Bruce Morland , author of Ferret, March 08, 1999
