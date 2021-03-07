Every day I write an update of my progress on 42, replying:

- What I did yesterday
- What am I going to do today
- What was my biggest obstacle

As soon as we make the dailies where I work.

# 2021-02-05

- Yesterday I configured my libft makefile and did 6 of the mandatory functions
- Today I plan to continue libft memory functions
- My biggest obstacle was the make documentation: it has several cryptic rules and 50 different ways to do the same thing.

# 2021-02-06

- Friday I advanced to the second part of libft, to the ft_split function.
- Today I plan to finish the second part of the libft and start the bonuses
- My biggest obstacle was knowing which corner cases the moulinette will test. I hope the automatic tests charge for everything.

# 2021-02-07

- Yesterday I finished all the mandatory functions of libft and started the bonus.
- Today I plan to finish the bonus and test everything on the guacamole.
- My biggest obstacle was ft_split: this function was very boring to implement. Ft_itoa was also very rough.

# 2021-02-08

- Yesterday I finished the libft bunus, corrected the tests that were failing and made the first correction.
- If I open a slot I plan to make the second correction today.
- This week and next I will take classes to get the license, and I will be unavailable after 7pm. My biggest obstacle is to find a correction slot before 7pm.

# 2021-02-09

- Yesterday I didn't do anything related to the 42's cursus.
- Today I'm going to do my second libft correction.
- My biggest obstacle is the classes to get the license: go from 19h to 23h. I'm coming home late.

# 2021-02-10

- Yesterday I did the second libft correction.
- If I have time, today I will install the vm to be able to make evaluations of other cadets and to earn points.
- My biggest obstacle in these last days has been time.

# 2021-02-11

- Yesterday I was unable to install the vm.
- Today I will do the third correction of libft.

# 2021-02-12

- Yesterday I finished the libft !!!
- If there is time, today I will start the get next line.

# 2021-02-14

- Yesterday I implemented unit tests with Unity on Libft (only 14 functions, WIP):
  - https://github.com/librity/ft_libft/tree/main/tests
- Today I'm starting get_next_line.
- I had no obstacles.

# 2021-02-15

- Yesterday I started get_next_line. I already have a good idea of ​​what to do. I am finding a way to advance the position of the file descriptor in `read`.
  I'm also trying to understand how I'm going to allocate enough memory for an entire line, since I can only read `BUFFER_SIZE` bytes at a time, and the line can be longer than this` BUFFER_SIZE`.
- Today I will not be able to code much for work and the CFC.
- My biggest obstacle was the lack of context: get_next_line is like a `getc` so it takes the entire line.

# 2021-02-16

- Yesterday I talked to @rdutenke, who asked me several questions about `get_next_line`:
  _Now I know that read advances the poetry in the file descriptor automatically._
  The "cat jump" for this project is to use a static pointer as a buffer, allocated with `BUFFER_SIZE + 1`: this way we can pass it to` read` and treat the different cases:

1. If the read buffer does not have `'\ n'` or` EOF`, we concatenate with the previous buffer and call `read` again.
2. If the read buffer has `'\ n'` we concatenate with the previous buffer up to`' \ n'`.
3. If the buffer read has `EOF`, we concatenate it with the previous buffer up to` EOF`.
4. Finally, we have to point the `line` pointer passed to an allocated string that contains the entire line without the` '\ n'`. Then we release the memory allocated in the intermediate strings and return `1` or` 0` to `'\ n'` or` EOF` respectively.
5. If the parameters have a problem (`BUFFER_SIZE <= 0`), or in any of these operations we are unable to allocate memory, we release all allocated memory and return` -1`.

- Today I will not be able to code much for work and the CFC.

# 2021-02-17

- Yesterday I was unable to dedicate myself to the project.
- Today I will not be able to code much for work and the CFC. At least it's my penultimate CFC day, and I'm going to get rid of it.

# 2021-02-18

- Yesterday I learned from @ viniseneda # 6780
  on how bitwise operations optimize the code: ~~ make comparisons with `|` instead of `||`. ~~ Modern compilers do several different optimizations, and these vary from compiler to compiler. The ideal is to analyze the generated assembly to know which optimizations are best for the compiler used:
  - https://stackoverflow.com/questions/52137520/when-use-bitwise-operations-instead-of-arithmetic-alternatives
  - https://github.com/agavrel/42-Bitwise_Operators
- Today is my last CFC day: partying_face :!

# 2021-02-19

- Yesterday I learned from @ viniseneda # 6780
  about the difference between arrays and pointers, between memory stack and heap, and about static and extern pointers.
  - https://stackoverflow.com/questions/29717970/do-i-need-to-free-char-array-of-fixed-length
  - https://vivadifferences.com/difference-between-stack-and-heap-in-c /
  - https://stackoverflow.com/questions/1286515/extern-and-static-pointers-in-c
- Today it will be possible to code!

# 2021-02-20

- Yesterday I left my get_next_line working!
- Today I'm going to refactor, keep it in tandem with the moulinette and run the github tests.
- My biggest difficulty is being to break the get_next_line into smaller functions as it has to pass a lot of references to the sub-functions.

# 2021-02-21

- Yesterday I refactored and corrected (almost) all the errors of get_next_line. I also created a script to facilitate the tests of the project:
  - https://github.com/librity/ft_get_next_line/blob/main/github_testers.sh
- Today I'm going to make get_next_line pass the missing tests and evaluate if it's worth making the bonus.
- My biggest obstacle was to open the automatic tests to see what was failing.

# 2021-02-22

- Yesterday I finished the get_next_line!
- Today I'm going to start netwhat, studying private ips, masks, DHCP and IPV6.

# 2021-02-23

- Yesterday I studied several concepts network concepts. I also made a call with my squad where I explained gnl, and wrote a condensed version of it:
  - https://github.com/librity/ft_get_next_line/blob/main/README.md
- I intend to put netwhat for correction today and finish it as soon as possible.

# 2021-02-24

- Yesterday I chipped on the netwhat test, and I will have to wait 3 days to try again: laughing:: tired_face:: rofl:
  Since I can't sign up for another project until I finish this one, I started printf on my own: I studied various arguments with `stdarg.h` and added some functions to my libft.
  The Git Workshop was awesome: the guy was a lot of mangia.
- I intend to continue printf, starting by defining a scalable structure for it.
- My biggest obstacle is the netwhat retry time.

# 2021-02-25

- Yesterday I continued studying about printf. It makes several `conversions` that we will have to implement, and for each` conversions` we still have to consider the flags (example: `% 06.2f`,`% 15.10s` and `% * d`). Initially I will structure my code in two parts:
  1. I will verify that the number of arguments passed corresponds to the number of `conversions` in the format string, and return an error (` -1`) otherwise.
  2. Perocrrate the format string, writing each character until it reaches a `conversion`. For each `conversion` I will generate a method that creates an allocated and properly formatted string: from there it is only to write the string, add the length in the character count and free the memory.

I chose to do this because it is simple, I will allocate as little memory as possible (avoid memory leaks), and I can reuse various libft functions. Base me on section 7.3 of `The Ansi C Programming Language`, where they give an example of printf with this structure.

My original idea was to do with split and join in the format string, which would require doing some crazy checks between strings, in addition to the question of memory.

I also learned about how to check typing in C. I am in doubt if we need to check if the types of the parameters match the format string: Do I need to return an error in `ft_printf ("% s ", 42);`?

Finally, I added github actions to my project, which automatically run testers in macos whenever I push the master. I based myself on this repository: - https://github.com/wblech/42_github_actions

- Today I will continue the printf, starting with the makefile.

- My biggest obstacle is still the netwhat retry time.

# 2021-02-26

- Yesterday I managed to make a good progress in printf: I already have a structured code that prints strings, chars and ints.
- Today I will continue the printf.
- My biggest obstacle is still the netwhat retry time.

# 2021-02-27

- Yesterday I did the Elixir track by NLW from Rocket Seat. I made a very basic payments api. It was the first time that I touched Elixir, and I loved the language. I learned several concepts and good functional programming practices that helped me with 42 projects.
  - https://github.com/librity/nlw_elixir
- Today I'm going to do the other two NLW tracks: Node and React. I will also do netwhat, and if I have time to continue working on printf.

# 2021-02-28

- Yesterday I finished netwhat and advanced on the NLW React track.
- Today I will continue the NLW tracks and work on printf.

# 2021-03-01

- Yesterday I finished the NLW tracks.
- Today I'm going to work at printf.

# 2021-03-02

- Yesterday I studied other technologies and I was unable to work in printf.
- Today I'm going to work at printf.

# 2021-03-03

- My printf is already printing hexadecimal and dot numbers.
- Today I'm going to work at printf.

# 2021-03-04

- Yesterday I made a ruby ​​CLI where I used printf to create a table view. I also helped another cadet to debug the gnl.
- Today I'm going to work at printf.

# 2021-03-05

- Yesterday I went to printf: debugged and refactored a lot. Ta getting a very nice structure, with isolated structs for each "module" of the program.
- Today I'm going to work on printf.

# 2021-03-06

- Yesterday I went to printf: my printf is already making all the flags except the wildcard `'*'`, which is the most difficult. I also learned that there are some settings that are in different headers depending on the system. An example is`ARG_MAX`, which have` limits.h`in macos, and`linux / limits.h` in linux.
  For portability reasons it is legal to check and include the appropriate header in the projects, especially for those who are doing it in linux.
- https://stackoverflow.com/questions/5919996/how-to-detect-reliably-mac-os-x-ios-linux-windows-in-c-preprocessor
- I hope to finish the printf by tomorrow.

```c
# include <limits.h>

# ifdef __linux__
# include <linux / limits.h>
# endif
```

# 2021-03-07

- Yesterday I decided to put all my daily updates on a statistical website with Hugo. I thought it was a good opportunity to learn the technology, and I'm really enjoying it. I also studied other things and I was not able to work much in printf.
- https://42devdiaries.netlify.app/pt/
- Today I will continue working on printf.
