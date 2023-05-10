## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:b3415e2370c025a924067cb08c32af70dcab6b8df5f5da24eb74948c0b56cb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull caddy@sha256:bf1f9b05cd873cf00fb889174804fc09871d536192e28ca79806d2ce06ac8be7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087375418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bf96c22a8f8ca00c7b1aa4ea6aa818aaecc66be8cc1041ca0e601e7a505371`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:04:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 May 2023 03:04:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 10 May 2023 03:05:45 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 May 2023 03:05:46 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 May 2023 03:05:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 May 2023 03:05:47 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 10 May 2023 03:05:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 May 2023 03:05:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 May 2023 03:05:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 May 2023 03:05:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 May 2023 03:05:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 May 2023 03:05:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 May 2023 03:05:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 May 2023 03:05:54 GMT
EXPOSE 80
# Wed, 10 May 2023 03:05:55 GMT
EXPOSE 443
# Wed, 10 May 2023 03:05:55 GMT
EXPOSE 443/udp
# Wed, 10 May 2023 03:05:56 GMT
EXPOSE 2019
# Wed, 10 May 2023 03:07:04 GMT
RUN caddy version
# Wed, 10 May 2023 03:07:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667ccc021a0ffd29ac554311786b18ef3f4ce79304b32b3987c4b15d76740eb7`  
		Last Modified: Wed, 10 May 2023 03:11:20 GMT  
		Size: 452.1 KB (452128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9698181b72cdb77e36337a00405b68dda39d3d2cd554f8c58224bf449c9e6434`  
		Last Modified: Wed, 10 May 2023 03:11:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45ad734018db3b416d9411409fbf4b1fd962fc86b9f084f29178553e9a02893`  
		Last Modified: Wed, 10 May 2023 03:11:22 GMT  
		Size: 14.6 MB (14606465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fba1db5304dd13aa3c829c71db3499b7654768728d5ca7b6a614cea47117b80`  
		Last Modified: Wed, 10 May 2023 03:11:19 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bb775df753b9925f91b7a73e710b06b08c4bab0a4a99edf0207ec064cb7412`  
		Last Modified: Wed, 10 May 2023 03:11:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249cd1a03b939f74fd9fd25469cd0f680d23c21a538acd06e817e122ba76544c`  
		Last Modified: Wed, 10 May 2023 03:11:18 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb63434040f9b9d6731d4256c2260add6ef6abc2d76a373b93ba2c0ad1af1e`  
		Last Modified: Wed, 10 May 2023 03:11:17 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcc40645db58161e5f421fc5743065ea5b0b855b7f43e1ff7e56b89a9ad5ff`  
		Last Modified: Wed, 10 May 2023 03:11:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ae32c8eab142d3066a0e3a2cfdb1566684854bfbd41b881a369ba40644d733`  
		Last Modified: Wed, 10 May 2023 03:11:17 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9976933db5878bd15e571a3536a9599e7f03669308d0f8387483d1f2e64b04`  
		Last Modified: Wed, 10 May 2023 03:11:16 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05192cfb3bddb797a27af99f4b20f980ec3d66d94fb339aa5e05e7628458d0ba`  
		Last Modified: Wed, 10 May 2023 03:11:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b54eaa5aa52b3cbfe07b57bcf6db822d260bbe7d08a8b5831900ed9a0aa33f`  
		Last Modified: Wed, 10 May 2023 03:11:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91c50af884ce4981d30938663f16959a892f71f3ca95077dbc2e7466ce8250`  
		Last Modified: Wed, 10 May 2023 03:11:15 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87549b93f6723fa765b96b3f028e82cf7269edf04a813ceb908ef4ab0d8398c`  
		Last Modified: Wed, 10 May 2023 03:11:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3de8ba969ad5d4b84f4189ccbae6a41d8762556d6bdb747dbd96c17f4a36cc`  
		Last Modified: Wed, 10 May 2023 03:11:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe06f9a0fde1b305c1c1984e3c5d329e25ae772ad6d97aa8d831337008eb95dc`  
		Last Modified: Wed, 10 May 2023 03:11:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2d3002142e2b1d73a3caa9378851a440a5066afdfe4fbce0d782d12131f016`  
		Last Modified: Wed, 10 May 2023 03:11:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388f0b8cd9044e8da9a81b2b3521d00cbd4c9c3a5fc34bb930e933697b68c665`  
		Last Modified: Wed, 10 May 2023 03:11:14 GMT  
		Size: 258.9 KB (258943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc3ebc8e7d4a1c8f142db40262181ea8c803b37e889ccec8fda30d53a195541`  
		Last Modified: Wed, 10 May 2023 03:11:13 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
