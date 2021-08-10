
- [X] files that have same name across tree will show bugs!

- file add -> rename -> delete - issues somewhere in this flow



## DELETE ERROR

1) one at a time, open some files and makes changes and save them
2) create a new file
3) add some text and save
4) with file still open, delete the file using tree menu

file does not get deleted

5) refresh the browser
6) try to delete the file again

file is deleted, but "no file opened" screen shows up in editor and stays that way until another file is selected



## SERVICE SWITCH ERROR

1) open some files
2) switch project

expect: files should close
expect: settings stays open when switching?

actual: files stay open


## lingering settings

1) open a file
2) make changes
3) open settings
4) close settings

expect: file that is remaining shows its text
expect: settings body disappears

actaul: settings body shows for remaining file instead of file's text


## new file issue
1) create a file
2) file opens in editor

expect: file is selected in tree
expect: should show blank file contents

actual: editor says "no editable.."
actual: file is not selected in tree
