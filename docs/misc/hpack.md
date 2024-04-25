HPACK is a header compression format used in [[HTTP2|HTTP/2]] for reducing the size of headers. It's designed to minimize both the size of each individual header and the overall size of header sets, addressing redundancy across multiple requests. 

HPACK works by employing a static table of common [[HTTP headers]] (which both client and server know) and a dynamic table (which gets built during the session). This approach reduces the need to send repeated header frames. 

The format also includes [[Huffman Coding]] for compressing header values. The combination of these techniques makes HPACK effective in reducing overhead, which is particularly beneficial for mobile environments and applications where network efficiency is crucial.