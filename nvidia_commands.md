## Useful command list
- nvidia-smi
    - 要約情報
    オプション無しで実行
    - GPU一覧を取得する場合
    ``` bash
    nvidia-smi -L
    ```
    - 0番目のGPUの詳細情報を取得する場合
    ``` bash
    nvidia-smi -q -i 0
    ```
    - デバイスメモリ情報だけを表示する場合
    ``` bash
    nvidia-smi -q -i 0 -d MEMORY | tail -n 5
    ```
    - デバイスの利用状況だけを表示する場合
    ``` bash
    nvidia-smi -q -i 0 -d UTILIZATION | tail -n 4
    ```
- 特定のGPUを使いたい場合(環境変数を用いる方法)
    ``` bash
    CUDA_VISIBLE_DEVICES=<0~N-1の数値>
    ```
- サンプルを実行する場合
    - `/usr/local/cuda/samples/`以下でmakeしてみること
    
``` bash
Mon Jan 25 00:49:32 2021       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 455.45.01    Driver Version: 455.45.01    CUDA Version: 11.1     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  Quadro M2000M       On   | 00000000:01:00.0  On |                  N/A |
| N/A   52C    P5    N/A /  N/A |    266MiB /  4035MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      1294      G   /usr/lib/xorg/Xorg                 58MiB |
|    0   N/A  N/A      1899      G   /usr/lib/xorg/Xorg                119MiB |
|    0   N/A  N/A      2184      G   /usr/bin/gnome-shell               37MiB |
|    0   N/A  N/A      9954      G   /usr/lib/firefox/firefox           39MiB |
+-----------------------------------------------------------------------------+
```
