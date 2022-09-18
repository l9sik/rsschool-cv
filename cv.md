 # Ilya Poluectov
* email: poluectovilya3@icloud.com

* telegram: @poluectov_ilya

* vk: @poluns

* discord: l9sik(@l9sik)
# About myself
Hard-working entry-level software engineer. Completed 3 self projects including statistic informational program that now used in Gomel's psychological center. One of my programs is used in online auto-parts store. My goal is my own company. Always strive for new hights.
    
## Education

* 2021: BSUIR (Minks, Belarus). Expect to graduate in 2025
* 2022: RS-School JavaScript/Front-end 2022Q3. Expect to complete in 2023

# Skills
## Languages
* Java
* C++
* C
* Assembly(Fasm)
* Delphi
## Technologies
* Gitub
## Design tools
* Adobe Photoshop
* Adobe Illustrator
* Adobe Animate

## Code example
```
/*
Finds the length of pisano cycle.
In that realisation the fibonacci numbers starts from 0, 1, 1, 2, ...

@params m divident for fibnacci elements
*/
int pisano(int m) {
        if (m == 1) return 1;
        if (m == 2) return 3;

        // [6 * m] is the largest pisano cycle possible
        int[] fibo = new int[6 * m];
        int[] pisano = new int[6 * m];
        // constants
        fibo[0] = 0; pisano[0] = 0;
        fibo[1] = 1; pisano[1] = 1;
        fibo[2] = 1; pisano[2] = 1;
        int i;
        for (i = 3; i < fibo.length; i++) {
            fibo[i] = fibo[i - 1] + fibo[i - 2];
            pisano[i] = fibo[i] % m;
            //the first 0 after 0 1 combination
            if (pisano[i - 1] == 0) {
                // (i - 1) is the distance between 0s
                if ((i - 1) % 2 == 1) {
                    return (i - 1) * 4;
                } else if (pisano[i] == 1) {
                    return (i - 1);
                } else return (i - 1) * 2;
            }
        }
        return -1;
    }
```
# Projects
* [This cv](https://github.com/l9sik/rsschool-cv/blob/gh_pages/cv.md)