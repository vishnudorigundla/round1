# round1
## Problem statement :
Rotate a String Left by K Positions Write a program to rotate a given string s left by k positions 
without using any built-in string functions. For example, rotating "abcdef" by 2 would give "cdefab". 
Instructions: Do not use built-in rotation or substring functions. Implement the logic manually.
## Program :
```
package main
import (
"fmt"
)
func rotateleft(s []rune, l int, n int) []rune {
l = l % n
rotatedstring := make([]rune, n)
index := 0
for i := l; i < n; i++ {
rotatedstring[index] = s[i]
index++
}
for i := 0; i < l; i++ {
rotatedstring[index] = s[i]
index++
}
return rotatedstring
}
func main() {
var s string
var l, n int
fmt.Print("Enter the string: ")
fmt.Scan(&s)
runeslice := []rune(s)
fmt.Print("Enter the number of positions to rotate left: ")
fmt.Scan(&l)
n = 0
for range runeslice {
n++
}
rotated := rotateleft(runeslice, l, n)
fmt.Print("Rotated String: ")
for _, r := range rotated {
fmt.Print(string(r))
}
fmt.Println()
}
```
## outputs :
```
Sample input and outputs :
1. Enter the string: abcedf
 Enter the number of positions to rotate left: 2
 Rotated String: cedfab
2. Enter the string: adefgc
 Enter the number of positions to rotate left: 3
 Rotated String: fgcade
3. Enter the string: tfdsaw
 Enter the number of positions to rotate left: 4
 Rotated String: awtfds
```
![image](https://github.com/user-attachments/assets/5609301d-0282-4676-9c9e-4a70a27d5a9c)
![image](https://github.com/user-attachments/assets/e0e8c547-615a-43fc-9f0d-80c4d3f9e8b4)
## Result :
Therefore,the go program is executed successfully.
