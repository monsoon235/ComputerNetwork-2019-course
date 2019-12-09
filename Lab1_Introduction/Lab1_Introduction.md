# Computer Networking Lab -- Introduction

## 1. List up to 10 different protocols that appear in the protocol column in the unfiltered packet-listing window in step 7 above.

1. ARP
2. HTTP
3. OICQ
4. TCP
5. UDP
6. TLS
7. SSDP
8. DNS
9. BROWSER
10. FTP

## 2. How long did it take from when the HTTP GET message was sent until the HTTP OK reply was received?

测试 10 次请求 http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html, 得到的结果如下：

| Frequency | Response time (s) |
| --------- | ----------------- |
| 1         | 0.302526000       |
| 2         | 0.494395000       |
| 3         | 0.304560000       |
| 4         | 0.293132000       |
| 5         | 0.382363000       |
| 6         | 0.409553000       |
| 7         | 0.410033000       |
| 8         | 0.256819000       |
| 9         | 0.427050000       |
| 10        | 0.443600000       |
| Average   | 0.3724031         |

## 3. What is the Internet address of the gaia.cs.umass.edu (also known as wwwnet.cs.umass.edu)? What is the Internet address of your computer?

gaia.cs.umass.edu: 128.119.245.12

My computer: 192.168.43.160

## 4. Print the two HTTP messages displayed in step 9 above.

### Send

```pseudocode
Hypertext Transfer Protocol
    GET /wireshark-labs/INTRO-wireshark-file1.html HTTP/1.1\r\n
        [Expert Info (Chat/Sequence): GET /wireshark-labs/INTRO-wireshark-file1.html HTTP/1.1\r\n]
            [GET /wireshark-labs/INTRO-wireshark-file1.html HTTP/1.1\r\n]
            [Severity level: Chat]
            [Group: Sequence]
        Request Method: GET
        Request URI: /wireshark-labs/INTRO-wireshark-file1.html
        Request Version: HTTP/1.1
    Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8\r\n
    Accept-Language: zh-CN\r\n
    Upgrade-Insecure-Requests: 1\r\n
    User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/70.0.3538.102 Safari/537.36 Edge/18.18362\r\n
    Accept-Encoding: gzip, deflate\r\n
    Host: gaia.cs.umass.edu\r\n
    DNT: 1\r\n
    Connection: Keep-Alive\r\n
    \r\n
    [Full request URI: http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html]
    [HTTP request 1/1]
    [Response in frame: 1638]
```

### Receive

```pseudocode
Hypertext Transfer Protocol
    HTTP/1.1 200 OK\r\n
        [Expert Info (Chat/Sequence): HTTP/1.1 200 OK\r\n]
            [HTTP/1.1 200 OK\r\n]
            [Severity level: Chat]
            [Group: Sequence]
        Response Version: HTTP/1.1
        Status Code: 200
        [Status Code Description: OK]
        Response Phrase: OK
    Date: Wed, 11 Sep 2019 18:01:54 GMT\r\n
    Server: Apache/2.4.6 (CentOS) OpenSSL/1.0.2k-fips PHP/5.4.16 mod_perl/2.0.10 Perl/v5.16.3\r\n
    Last-Modified: Wed, 11 Sep 2019 05:59:02 GMT\r\n
    ETag: "51-59240b7c1a574"\r\n
    Accept-Ranges: bytes\r\n
    Content-Length: 81\r\n
        [Content length: 81]
    Keep-Alive: timeout=5, max=100\r\n
    Connection: Keep-Alive\r\n
    Content-Type: text/html; charset=UTF-8\r\n
    \r\n
    [HTTP response 1/1]
    [Time since request: 0.308088000 seconds]
    [Request in frame: 1629]
    [Request URI: http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html]
    File Data: 81 bytes
Line-based text data: text/html (3 lines)
    <html>\n
    Congratulations!  You've downloaded the first Wireshark lab file!\n
    </html>\n
```
