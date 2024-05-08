Buffer overflows are a type of vulnerability that occur in software when a program attempts to write more data to a buffer (a contiguous block of memory allocated to store data) than it can hold. This can lead to unexpected behavior and security vulnerabilities.

A buffer is a region of memory used to temporarily store data while being moved from one place to another. Buffers are often used when handling data streams or user input.

Many programming languages use fixed-size buffers. When a program writes more data to a buffer than it can hold, the excess data can overlfow into adjacent memory areas.

Buffer overflows typically occur because of insufficient bounds checking during data copying or manipulation operations. The simplest effect of a buffer overflow is a program crash.

More critically, buffer overflows can be exploited to execute arbitrary code. 

Web forms, [Uniform Resource Locator|URL]() parameters and [HTTP Headers]() are common input vectors in web app pentesting. Attackers may try to overflow buffers by providing excessively long input strings in these fields.

Pentesters also often use fuzzing techniques like [Directory Fuzzing]() or [Parameter Fuzzing (KB)](), sending large amounts of data or specifically crafted payloads to test how the app handles it.