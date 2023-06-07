* Chose you adventure
  * linking with pipe and output
    * cat
      * cat | head
        * cat | head
        * cat | head -n 15
      * cat | tail
        * cat | tail -n 20
        * cat | tail -f
          * tail -f "pattern" bigLogfile.txt | grep >> filtered.txt 
            * tail -f filtered.txt
            * open new terminal and do echo "more lines added with or without pattern" >> bigLogFile.txt 
      * cat | grep 
    * head > out.txt 
    * head >> outCont.txt
    * grep | sort
    * grep | sort | uniq 
    * grep | sort | uniq -c
      * grep | sort | uniq -c | sort -n
      * grep | sort | uniq -c | sort -nr
      * grep | sort | uniq -c | sort -nrk 1
  * grep 
    * grep , grep -E, grep -P : 
      * grep -E cant use non-greedy quantifiers
      * grep -P can't use \< or \> , only \b
        * regEx in VS Code 
    * grep -c
    * grep -v 
    * grep -A, grep -B, grep -C
    * RegEx syntax
      * character classes
        * digits
        * mixing digits and literal
          * find all "years"
      * quantifiers
        * exact number 
        * ranges
        * shorthands for 0-1, 0-, 1- 
        * NOTE: quantifiers are normally "greedy". Only the "-P style" (as opposed to "-E style") can make them non-greedy.
        * find all ip-addresses
        * find all URLs
      3. Anchors
        * beginning or end of line
        * beginning or end of "word"
      4. catching just the matched part of the line
        * grep -o
        * non-catching part of pattern
        * lookahead and lookbehind, defining what's before and after the thing to match, without catching
  * the awk util
    * awk '{ print $2 " " $NF }'
    * awk '{ print $(NF-1) }'
    * awk -F ";"
    * grep | sort | uniq -c | sort -nrk 1 | awk '{ print $(NF-1) }'
