# Commands
General Commands usefull in daily software development work

Find and Process running on a specific port Unix

    kill -9 `sudo netstat -lnpt | grep -i -n ":3000" | awk -F" " '{print $7}' | awk -F"/" '{print $1}'`


Find Process running on a specific port Windows

    netstat -aon | find /i "listening" | netstat -ano | findstr :4000

Kill process in Windows

    taskkill /PID 26148 /F

Find Process running on a specific port Macbook

    lsof -i tcp:3000
    netstat -vanp tcp | grep 3000
    
Kill process in Macbook
    
    kill -9 <PID>

Start a http server i Python

    python3 -m http.server 8888

Convert between Encodings
    
    iconv -f utf-16le -t utf-8 /mnt/c/Users/20250819120830/data.csv | awk -F',' '$7 ~ /793007/'
