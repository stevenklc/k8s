# microk8s
| 先以輕量級的來練習
| 官方建議4G RAM

* 使用VPS
  * AWS lightsail
    * 使用 5 usd 機器的來練習
    ```shell
    # 安裝
    sudo snap install microk8s --classic

    # 權限設置
    sudo usermod -a -G microk8s $USER
    sudo chown -f -R $USER ~/.kube

    # 啟動microk8s
    microk8s status --wait-ready
    # 1GB RAM完全跑不動