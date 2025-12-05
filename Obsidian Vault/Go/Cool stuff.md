
var arr[...]int{1,2,3,4,5} use ... to make a fixed arr of length however much stuff you add inside {}
i.e. this will be a fixed arr of size 5

arrays are fixed length while slices are variable length

arrays are pass by value , slices are pass by refrence

short hand declaration operator := can only be used within functions otherwise you need var format for package level declarations

package level init() func that runs only ONCE on package init (gets called before main)W