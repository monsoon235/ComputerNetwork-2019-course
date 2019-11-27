# Computer Networking Lab -- HTTP

## 1. Is your browser running HTTP version 1.0 or 1.1? What version of HTTP is the server running?

My browser runs HTTP 1.1

Server runs HTTP 1.1

## 2. What languages (if any) does your browser indicate that it can accept to the server?

Accept simplified Chinese(zh-CN), English(en) and traditional Chinese(zh-TW).

```pseudocode
Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,zh-TW;q=0.7
```

## 3. What is the IP address of your computer? Of the gaia.cs.umass.edu server?

My compurt: `202.141.181.193`

`gaia.cs.umass.edu` Server: `128.119.245.12`

## 4. What is the status code returned from the server to your browser?

200

```pseudocode
Status Code: 200
```

## 5. When was the HTML file that you are retrieving last modified at the server?

19 Sep 2019 05:59:01

```pseudocode
Last-Modified: Thu, 19 Sep 2019 05:59:01 GMT
```

## 6. How many bytes of content are being returned to your browser?

128 bytes.

```pseudocode
Content-Length: 128
```

## 7. By inspecting the raw data in the packet content window, do you see any headers within the data that are not displayed in the packet-listing window? If so, name one.

None.

## 8. Inspect the contents of the first HTTP GET request from your browser to the server. Do you see an “IF-MODIFIED-SINCE” line in the HTTP GET?

No.

## 9. Inspect the contents of the server response. Did the server explicitly return the contents of the file? How can you tell?

Yes. If there is no `“IF-MODIFIED-SINCE` in HTTP request from client, server always returns the latest content of file.

## 10. Now inspect the contents of the second HTTP GET request from your browser to the server. Do you see an “IF-MODIFIED-SINCE:” line in the HTTP GET? If so, what information follows the “IF-MODIFIED-SINCE:” header?

```pseudocode
If-Modified-Since: Thu, 19 Sep 2019 05:59:01 GMT
```

Yes. The last modified time (`Last_Modified`) in OK trun message which the browser get from server.

## 11. What is the HTTP status code and phrase returned from the server in response to this second HTTP GET? Did the server explicitly return the contents of the file? Explain.

State code and phrase:

```pseudocode
304 Not Modified
```

Server didn't explicity return thr contents of the file, because the browser cached the file.

## 12. How many HTTP GET request messages did your browser send? Which packet number in the trace contains the GET message for the Bill or Rights?

Only 1 HTTP GET request.

The 1st packet.

## 13. Which packet number in the trace contains the status code and phrase associated with the response to the HTTP GET request?

The 1st packet.

## 14. What is the status code and phrase in the response?

```pseudocode
200 OK
```

## 15. How many data-containing TCP segments were needed to carry the single HTTP response and the text of the Bill of Rights?

4 TCP segments.

## 16. How many HTTP GET request messages did your browser send? To which Internet addresses were these GET requests sent?

2 HTTP GET requests.

`128.119.245.12`

## 17. Can you tell whether your browser downloaded the two images serially, or whether they were downloaded from the two web sites in parallel? Explain.

Serially. 2 HTTP GET request for pictures are almost sent at the same time, and the arrival times of responses varies depending on the file size, network state, etc.

## 18. What is the server’s response (status code and phrase) in response to the initial HTTP GET message from your browser?

```pseudocode
401 Unauthorized
```

## 19. When your browser’s sends the HTTP GET message for the second time, what new field is included in the HTTP GET message?

```pseudocode
Authorization: Basic d2lyZXNoYXJrLXN0dWRlbnRzOm5ldHdvcms=
```
