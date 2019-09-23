.. _getting_started-installation:

============
安装
============

Snakemake可以通过PyPi以及Bioconda安装，也可以从源代码安装。
您可以使用以下方法安装Snakemake。

.. _conda-install:

Conda安装
======================

这是安装Snakemake的推荐方法，因为它还使Snakemake能够 :ref:`处理工作流程的软件依赖` 。

首先，安装Miniconda Python3发行版。请参阅 `此处 <https://conda.io/docs/install/quick.html>`_ 获取安装说明。确保

* 安装 **Python3** 版本你的Miniconda;
* 将conda加入环境变量

然后，安装Snakemake

.. code-block:: console

    $ conda install -c bioconda -c conda-forge snakemake

来自 `Bioconda <https://bioconda.github.io>`_ channel。可以安装最小版本的Snakemake

.. code-block:: console

    $ conda install -c bioconda -c conda-forge snakemake-minimal

出于历史，可重复性和连续性的原因，可以通过Bioconda获得Snakemake。但是，可以使用其它channel安装Snakemake，比如在包名字前加上前缀 ``::bioconda``, 比如，

.. code-block:: console

    $ conda install -c conda-forge bioconda::snakemake bioconda::snakemake-minimal

全局安装
===================

使用Python ``>=3.5``，可以通过以下命令来安装Snakemake

.. code-block:: console

    $ easy_install3 snakemake

或

.. code-block:: console

    $ pip3 install snakemake


虚拟环境安装
========================

在虚拟环境中创建安装，使用以下命令：

.. code-block:: console

    $ virtualenv -p python3 .venv
    $ source .venv/bin/activate
    $ pip install snakemake


源码安装
======================

建议将Snakemake安装到virtualenv中，而不是全局安装。使用以下命令创建一个虚拟环境并安装Snakemake。请注意，这将安装开发版本，并且在您从源代码进行安装时，相信您知道自己做法以及如何查看各个版本/标签。

.. code-block:: console

    $ git clone https://bitbucket.org/snakemake/snakemake.git
    $ cd snakemake
    $ virtualenv -p python3 .venv
    $ source .venv/bin/activate
    $ python setup.py install

还可以使用 ``python setup.py develop``来安装开发版，在该安装中，并不复制文件，而是创建了链接，并且源代码中的更改在snakemake命令中立即可见。
