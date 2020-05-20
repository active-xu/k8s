FROM ubuntu:18.04
# 更新软件源（这里用的是中科大的源，因为阿里云的源有个依赖无法下载）
RUN echo 'deb http://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse' > /etc/apt/sources.list && \
    echo 'deb http://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse' >> /etc/apt/sources.list && \
    echo 'deb http://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse' >> /etc/apt/sources.list && \
    echo 'deb http://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse' >> /etc/apt/sources.list && \
    echo 'deb http://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse' >> /etc/apt/sources.list && \
    apt-get update
# 安装所需依赖
RUN apt-get install -y vim wget python2.7 ping inetutils-ping python-pip redis-tools dnsutils
# 安装 Redis Trib，注意默认安装版本为 0.6.1 是有 BUG 的
RUN pip install redis-trib==0.5.1
