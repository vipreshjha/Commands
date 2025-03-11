# Commands
General Commands usefull in daily software development work

Find and Process running on a specific port Unix
    kill -9 `sudo netstat -lnpt | grep -i -n ":3000" | awk -F" " '{print $7}' | awk -F"/" '{print $1}'`


Find Process running on a specific port Windows
    netstat -aon | find /i "listening" | netstat -ano | findstr :4000

Kill process in Windows
    taskkill /PID 26148 /F

Start a http server i Python
    python3 -m http.server 8888

