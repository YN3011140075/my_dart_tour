# 使用 VSCode 官方的 Ubuntu 基础镜像
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# 安装必要的软件
RUN apt-get update && apt-get install -y apt-transport-https wget ca-certificates

# 添加 Google GPG 公钥
RUN wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | gpg --dearmor -o /usr/share/keyrings/dart.gpg

# 添加 Dart 软件源
RUN echo 'deb [signed-by=/usr/share/keyrings/dart.gpg] https://storage.googleapis.com/download.dartlang.org/linux/debian stable main' > /etc/apt/sources.list.d/dart_stable.list

# 安装 Dart
RUN apt-get update && apt-get install -y dart
