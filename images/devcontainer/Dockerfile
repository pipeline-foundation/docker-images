FROM mcr.microsoft.com/vscode/devcontainers/base:0.202.2-alpine3.14

RUN apk update; \
	apk add --no-cache \
		ca-certificates \
		less \
		ncurses-terminfo-base \
		krb5-libs \
		libgcc \
		libintl \
		libssl1.1 \
		libstdc++ \
		tzdata \
		userspace-rcu \
		zlib \
		icu-libs \
		curl; \
	apk -X https://dl-cdn.alpinelinux.org/alpine/edge/main add --no-cache \
    lttng-ust; \
	curl -L https://github.com/PowerShell/PowerShell/releases/download/v7.1.5/powershell-7.1.5-linux-alpine-x64.tar.gz -o /tmp/powershell.tar.gz; \
	mkdir -p /opt/microsoft/powershell/7; \
	tar zxf /tmp/powershell.tar.gz -C /opt/microsoft/powershell/7; \
	chmod +x /opt/microsoft/powershell/7/pwsh; \
	ln -s /opt/microsoft/powershell/7/pwsh /usr/bin/pwsh

# Built with ❤ by [Pipeline Foundation](https://pipeline.foundation)