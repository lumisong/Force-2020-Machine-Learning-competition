# 数据分析环境

初始数据分析python环境创建。使用Python插件包进行管理，安装的环境在.conda目录下

## 配置环境问题

在环境下直接使用conda进行install

```shell
conda install -c conda-forge pandas
conda install -c conda-forge matplotlib
conda install -c conda-forge scikit-learn
```

1. conda环境在 Python环境管理器中不显示了。
2. 使用交互操作时，出现了很多意想不到的问题，--json 可能是这个出现导致的问题。

![conda环境不显示](./fig_env_md/2024-02-22-16-07-23.png)

安装问题，版本不兼容，最近的Python版本与pandas版本不兼容问题。安装pandas安装不上。

```shell
> conda update --all -p ./.conda
> conda update --all -d -p ./.conda --json
> conda list -p ./.conda --json

```

出现错误(待解决)

```text
ebug: conda update --all -d -p /home/lumisong/文档/Force-2020-Machine-Learning-competition-master/.conda --json: {
  "message": "All requested packages already installed.",
  "success": true
}

Error: Failed to get latest package information for /home/lumisong/文档/Force-2020-Machine-Learning-competition-master/.conda/bin/python) TypeError: Cannot read properties of undefined (reading 'UNLINK')
    at getOutdatedCondaPackages (/home/lumisong/.vscode/extensions/donjayamanne.python-environment-manager-1.2.4/out/client/extension.js:19757:13)
    at processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async Promise.all (index 1)
    at getOutdatedPackages (/home/lumisong/.vscode/extensions/donjayamanne.python-environment-manager-1.2.4/out/client/extension.js:19122:46)
```
对比：直接Terminal中操作，不使用--json参数，更新

```shell

conda update --all -p ./.conda

```

Warning 警告信息

```text

==> WARNING: A newer version of conda exists. <==
  current version: 4.12.0
  latest version: 24.1.2

Please update conda by running

    $ conda update -n base -c defaults conda

```

环境位置

```text



## Package Plan ##

  environment location: /home/lumisong/文档/Force-2020-Machine-Learning-competition-master/.conda


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    mkl-2023.1.0               |   h213fc3f_46344       171.5 MB  http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
    ------------------------------------------------------------
                                           Total:       171.5 MB

```

```text

The following NEW packages will be INSTALLED:

  importlib-metadata anaconda/pkgs/main/linux-64::importlib-metadata-7.0.1-py38h06a4308_0
  importlib_metadata anaconda/pkgs/main/noarch::importlib_metadata-7.0.1-hd3eb1b0_0
  zipp               anaconda/pkgs/main/linux-64::zipp-3.17.0-py38h06a4308_0

```

```text

The following packages will be REMOVED:

  entrypoints-0.4-pyhd8ed1ab_0
  prompt_toolkit-3.0.42-hd8ed1ab_0

```

```text

The following packages will be UPDATED:

  ipython            conda-forge/noarch::ipython-8.12.0-py~ --> anaconda/pkgs/main/linux-64::ipython-8.12.2-py38h06a4308_0
  jupyter_client     conda-forge/noarch::jupyter_client-7.~ --> anaconda/pkgs/main/linux-64::jupyter_client-8.6.0-py38h06a4308_0
  prompt-toolkit     conda-forge/noarch::prompt-toolkit-3.~ --> anaconda/pkgs/main/linux-64::prompt-toolkit-3.0.43-py38h06a4308_0
  ptyprocess         conda-forge::ptyprocess-0.7.0-pyhd3de~ --> anaconda/pkgs/main::ptyprocess-0.7.0-pyhd3eb1b0_2
  six                  conda-forge::six-1.16.0-pyh6c4a22f_0 --> anaconda/pkgs/main::six-1.16.0-pyhd3eb1b0_1
  tornado            conda-forge::tornado-6.1-py38h0a891b7~ --> anaconda/pkgs/main::tornado-6.3.3-py38h5eee18b_0
  typing_extensions  conda-forge/noarch::typing_extensions~ --> anaconda/pkgs/main/linux-64::typing_extensions-4.9.0-py38h06a4308_1

```

```

The following packages will be SUPERSEDED by a higher-priority channel:

  backcall           conda-forge::backcall-0.2.0-pyh9f0ad1~ --> anaconda/pkgs/main::backcall-0.2.0-pyhd3eb1b0_0
  blas                                            pkgs/main --> anaconda/pkgs/main
  brotli-python                                   pkgs/main --> anaconda/pkgs/main
  ca-certificates                                 pkgs/main --> anaconda/pkgs/main
  certifi                                         pkgs/main --> anaconda/pkgs/main
  charset-normalizer                              pkgs/main --> anaconda/pkgs/main
  decorator          conda-forge::decorator-5.1.1-pyhd8ed1~ --> anaconda/pkgs/main::decorator-5.1.1-pyhd3eb1b0_0
  idna                                            pkgs/main --> anaconda/pkgs/main
  intel-openmp                                    pkgs/main --> anaconda/pkgs/main
  joblib                                          pkgs/main --> anaconda/pkgs/main
  libgfortran-ng                                  pkgs/main --> anaconda/pkgs/main
  libgfortran5                                    pkgs/main --> anaconda/pkgs/main
  matplotlib-inline  conda-forge/noarch::matplotlib-inline~ --> anaconda/pkgs/main/linux-64::matplotlib-inline-0.1.6-py38h06a4308_0
  mkl                                             pkgs/main --> anaconda/pkgs/main
  mkl-service                                     pkgs/main --> anaconda/pkgs/main
  mkl_fft                                         pkgs/main --> anaconda/pkgs/main
  mkl_random                                      pkgs/main --> anaconda/pkgs/main
  nest-asyncio       conda-forge/noarch::nest-asyncio-1.6.~ --> anaconda/pkgs/main/linux-64::nest-asyncio-1.6.0-py38h06a4308_0
  numpy                                           pkgs/main --> anaconda/pkgs/main
  numpy-base                                      pkgs/main --> anaconda/pkgs/main
  openssl                                         pkgs/main --> anaconda/pkgs/main
  parso               conda-forge::parso-0.8.3-pyhd8ed1ab_0 --> anaconda/pkgs/main::parso-0.8.3-pyhd3eb1b0_0
  pickleshare        conda-forge::pickleshare-0.7.5-py_1003 --> anaconda/pkgs/main::pickleshare-0.7.5-pyhd3eb1b0_1003
  pooch                                           pkgs/main --> anaconda/pkgs/main
  pure_eval          conda-forge::pure_eval-0.2.2-pyhd8ed1~ --> anaconda/pkgs/main::pure_eval-0.2.2-pyhd3eb1b0_0
  pysocks                                         pkgs/main --> anaconda/pkgs/main
  python-dateutil    conda-forge::python-dateutil-2.8.2-py~ --> anaconda/pkgs/main::python-dateutil-2.8.2-pyhd3eb1b0_0
  requests                                        pkgs/main --> anaconda/pkgs/main
  scikit-learn                                    pkgs/main --> anaconda/pkgs/main
  scipy                                           pkgs/main --> anaconda/pkgs/main
  tbb                                             pkgs/main --> anaconda/pkgs/main
  threadpoolctl                                   pkgs/main --> anaconda/pkgs/main
  urllib3                                         pkgs/main --> anaconda/pkgs/main


Proceed ([y]/n)? y

```

```text

Downloading and Extracting Packages
mkl-2023.1.0         | 171.5 MB  | ########################################################################################### | 100% 
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

```

pandas 安装过程中的问题

您在尝试安装的 pandas 版本（2.1.4）与您当前环境中的 Python 版本（3.8）不兼容。根据错误信息，pandas 2.1.4 需要 Python 版本 3.9、3.10、3.11 或 3.12。

此外，pandas 2.1.4 还需要 glibc 版本至少为 2.17，而您当前的 glibc 版本为 2.31，这可能也是导致问题的原因。

您可以尝试安装与您的 Python 版本兼容的 pandas 版本，或者升级您的 Python 版本以匹配 pandas 2.1.4 的需求。

例如，如果您想要安装与 Python 3.8 兼容的 pandas 版本，您可以运行以下命令：

conda install pandas

这将会安装最新的、与您当前 Python 版本兼容的 pandas 版本。
