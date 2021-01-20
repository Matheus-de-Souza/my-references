# Misc

[Go Back](./)

## Sed Tricks

### Filter and save a new file

Filter the file `marketing.txt` by gmail accounts and save results in `novo.txt`.

`sed -n '/gmail.com/ w novo.txt' marketing.txt`

ou

`cat marketing.txt | sed -n '/gmail.com/ w novo.txt'`

### Remove HTML tags

`echo '<a href="#">Link aqui</a><br/>' | sed 's/<[^>]*>//g'`

Result: Link aqui

### Kill Finder (MacOS)

https://www.howtogeek.com/259378/how-to-quit-the-finder-in-os-x/
