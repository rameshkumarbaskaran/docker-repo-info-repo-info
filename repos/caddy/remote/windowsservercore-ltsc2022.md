## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:113f187a1100da96770eeaecc6e118b4be7ef33cb4d01611de3e3045ed3a4acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
