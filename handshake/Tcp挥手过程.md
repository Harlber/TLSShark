# TCP close过程

<img src="wave_all.png" width="800px" />

序号14～20的`segment`展示了tcp关闭通道的过程

`segment 14`

<img src="14.png" width="800px" />

`segment 15`

<img src="15.png" width="800px" />

`segment 16`

<img src="16.png" width="800px" />

`segment 17`

<img src="17.png" width="800px" />

`segment 18`

<img src="18.png" width="800px" />

`segment 19`

<img src="19.png" width="800px" />

`segment 20`

<img src="20.png" width="800px" />

## 图示
| 方向                        | Sequence number   |Acknowledgment number|Next Sequence number |Tcp Flags|
| -------------------------- | ----------------------- |---------------------|---------------------|---------------|
|         -->               | 1             |1|31|PSH ACK|
|         <--               | 1             |31|27|PSH ACK|
|         <--               | 27         |31|27|FIN|
|         -->               | 31           |27|31|ACK|
|         -->               | 31 |28|31|ACK|
|         -->               | 31           |28|31|FIN|
|         <--               | 28           |32|28|ACK|

左边为client，右边为server