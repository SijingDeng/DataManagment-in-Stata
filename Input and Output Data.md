Input: infile, insheet, infix, use, xmluse

## Data with delimiter "tab"
   type d11.txt
   * check the type of the file
   insheet v1 v2 v3 using d11.txt, clear

## Data with delimiter "blank"
   insheet using d21.txt, clear delimiter(" ")
   * need to claim the type of delimiter
   infile v1 v2 v3 using d21.txt, clear
   
## Data with string
   * need to 
  