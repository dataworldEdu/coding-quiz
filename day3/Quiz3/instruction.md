#### ๐ค ๋ฌธ์  ์ค๋ช
๋ฏธ๋ก์ 2D ๋ฐฐ์ด๊ณผ ๊ธธ์ ๋ฐฐ์ด์ด ์ฃผ์ด์ง๋ค. 

๋น์ ์ ์๋ฌด๋ ์ฃผ์ด์ง ์ง์๋ฅผ ๋ฐ๋ผ ์ข๋ฃ ์ง์ ์ ๋๋ฌํ๋ฉด 'Finish'๋ฅผ ๋ฐํ ํ๋ค. 

๋ง์ฝ ์ด๋ค ๋ฒฝ์ ๋ถ๋ชํ๊ฑฐ๋ ๋ฏธ๋ก ๊ฒฝ๊ณ์  ๋ฐ์ผ๋ก ๋๊ฐ๋ค๋ฉด, ๋น์ ์ 'Dead'๋ฅผ ๋ฐํ ํ๋ค. 

๋ชจ๋  ๋์์ ๋ค ์จ๋๊ณ ๋ ์ฌ์ ํ ๋ฏธ๋ก ์์ ์๋ ์์ ์ ๋ฐ๊ฒฌํ๋ค๋ฉด 'Lost'๋ฅผ ๋ฐํ ํ๋ค.

maze = [[1,1,1,1,1,1,1],
        [1,0,0,0,0,0,3],
        [1,0,1,0,1,0,1],
        [0,0,1,0,0,0,1],
        [1,0,1,0,1,0,1],
        [1,0,0,0,0,0,1],
        [1,2,1,0,1,0,1]]

      0 = Safe place to walk
      1 = Wall
      2 = Start Point
      3 = Finish Point      

  direction = ["N","N","N","N","N","E","E","E","E","E"] == "Finish"

1. Maze ๋ฐฐ์ด์ ํญ์ ์ ์ฌ๊ฐํ์ผ ๊ฒ์ด๋ค. N x N ๊ทธ๋ฌ๋ ํฌ๊ธฐ ๋ฐ ํจ๋์ ํ์คํธ์์ ํ์คํธ๋ก ๋ณ๊ฒฝ๋๋ค.

2. ์ต์ข ์ํ์ ์ถ๋ฐ ์์น์ ๊ฒฐ์น ์์น๊ฐ ๋ฐ๋๋ค.

3. ๋ฐฉํฅ ๋ฐฐ์ด์ด ํญ์ ๋๋ฌธ์๋ก ๋์ด ์์ผ๋ฉฐ N = ๋ถ, E = ๋๋ถ, W = ์, S = ๋จ์ผ๋ก ๋์ด ์๋ค.

4. ๋ชจ๋  ๋์์ด ์ฌ๋ผ์ง๊ธฐ ์ ์ ๋์ ์ ๋๋ฌํ๋ฉด Finish๋ฅผ ๋ฐํํด์ผ ํ๋ค.

5. ์ด๋ค ๋ฒฝ์ ๋ถ๋ชํ๊ฑฐ๋ ๋ฏธ๋ก ๊ฒฝ๊ณ์  ๋ฐ์ผ๋ก ๋๊ฐ๋ฉด Dead๋ฅผ ๋ฐํ ํ๋ค.

6. ๋ชจ๋  ๋์์ ๋ค ์จ๋๊ณ ๋ ์ฌ์ ํ ๋ฏธ๋ก ์์ ์๋ ์์ ์ ๋ฐ๊ฒฌํ๋ฉด Lost๋ฅผ ๋ฐํ ํ๋ค.   

#### ๐ฏ TestCase
maze_runner(maze,["N","N","N","N","N","E","E","E","E","E"]), "Finish"
maze_runner(maze,["N","N","N","N","N","E","E","S","S","E","E","N","N","E"]), "Finish"
maze_runner(maze,["N","N","N","N","N","E","E","E","E","E","W","W"]), "Finish"