# # Use a Windows Server Core image as the base
# FROM mcr.microsoft.com/windows/servercore:ltsc2022

# # Install Chocolatey, a Windows package manager
# RUN powershell -Command "Set-ExecutionPolicy Bypass -Scope Process; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex"

# # Install Rust using Chocolatey
# RUN choco install -y rust

# # Set up the working directory
# WORKDIR C:\app

# # Set the command to run the application
# ENTRYPOINT ["cmd", "/c", "waitfor", "never-sent-event"]

FROM rust:latest

RUN apt-get update
RUN apt-get install mingw-w64
RUN rustup target add x86_64-pc-windows-gnu

WORKDIR /root

ENTRYPOINT ["tail", "-f", "/dev/null"]