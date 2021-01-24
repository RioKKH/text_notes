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

