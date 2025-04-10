# music-hash-refresher
用DeepSeek生成的一个纯前端音频hash修改器，在几乎不改变音频的情况下改变音频文件的hash

## 机理（BY deepseek-r1）

1. 用户通过网页上传MP3文件，前端校验格式。

2. 使用FileReader读取为ArrayBuffer。

3. 创建一个新的Uint8Array，比原文件大1字节。

4. 将原数据复制过去，最后一个字节设为0（或其他值）。

5. 生成新的Blob，提供下载链接。

6. 计算修改前后的哈希值，比如使用Web Crypto API的SHA-1或MD5，显示给用户。

## 趣事

从idea冒出来到上传到github库仅用时不到5分钟~
