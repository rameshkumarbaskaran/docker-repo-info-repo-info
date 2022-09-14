## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f04e196fed771d183af767ba332ca75979908b29329b52aff02770add0edaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull caddy@sha256:20ccce7c31b1a344d8f4c009976cf0cd187be951696d22e1917b1b5a602a781a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2362341980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83aa1d4c66bee282ceaf4730d4a698e3af18f052310d30d09d24c37c09240e9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:53:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Sep 2022 17:53:04 GMT
ENV CADDY_VERSION=v2.5.2
# Wed, 14 Sep 2022 17:53:25 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b104d364a458f457bab24f12f97470612035f705fceb170ce16b567e18e0429a18a726f6b1bb435f92d28a659aee52c08c0bac3be41b7f23887b8e7307507482')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Sep 2022 17:53:26 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Sep 2022 17:53:27 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Sep 2022 17:53:28 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Wed, 14 Sep 2022 17:53:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Sep 2022 17:53:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Sep 2022 17:53:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Sep 2022 17:53:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Sep 2022 17:53:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Sep 2022 17:53:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Sep 2022 17:53:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Sep 2022 17:53:35 GMT
EXPOSE 80
# Wed, 14 Sep 2022 17:53:36 GMT
EXPOSE 443
# Wed, 14 Sep 2022 17:53:36 GMT
EXPOSE 443/udp
# Wed, 14 Sep 2022 17:53:37 GMT
EXPOSE 2019
# Wed, 14 Sep 2022 17:53:57 GMT
RUN caddy version
# Wed, 14 Sep 2022 17:53:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670c7849c1d90324a53de61d6b35f7162d3a1682be8af63241025ca80eca41`  
		Last Modified: Wed, 14 Sep 2022 18:03:52 GMT  
		Size: 599.9 KB (599906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04306f23cf2ea41f15634845bb99e9cc62e4dddc9595cb0ba8674a6b562c204d`  
		Last Modified: Wed, 14 Sep 2022 18:03:51 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0b928a9cc23ca9704f5c43e673f13930892efa8c23c81d2c781fe856f201ca`  
		Last Modified: Wed, 14 Sep 2022 18:03:55 GMT  
		Size: 14.5 MB (14450087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8e658a04db74cab5d55a9f2cf3fc2a21e0c4060831540d776cae7b4064335`  
		Last Modified: Wed, 14 Sep 2022 18:03:50 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1d2b34563ffd9e369a4724d559bccee275f660f04cb0edce29ccaa65d6cb88`  
		Last Modified: Wed, 14 Sep 2022 18:03:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa7d63770e006a5f087b56bde9de40e6d7f62f8e3a67f09d57fbb7d41e06230`  
		Last Modified: Wed, 14 Sep 2022 18:03:48 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc4f1f2e9a9d2f9214b46d472e51d752aa0d38b2ae701d15e7ae2386e141a`  
		Last Modified: Wed, 14 Sep 2022 18:03:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa09c558f87a1a65cd54f8cd2cfe7cf2c5de3ed34e42b973f0b96bbb8ecaee0`  
		Last Modified: Wed, 14 Sep 2022 18:03:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5283655337e3eb8ca95d52fefdb579ac6a4ad81f0745df45b9a8cc318a2993`  
		Last Modified: Wed, 14 Sep 2022 18:03:48 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe17b2036fa533cea3770a4ef3cc18a9db8b0543374b338624edbd7fe1c0607`  
		Last Modified: Wed, 14 Sep 2022 18:03:46 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b471aa75a4f1bbadf78b44c53e75e87797ef727a92d89a491e3b16e03e9b94ca`  
		Last Modified: Wed, 14 Sep 2022 18:03:46 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5245c9c245470624ad7a002efc6aded7088fd9ef49e9b34b6e0afea5cb6d00c6`  
		Last Modified: Wed, 14 Sep 2022 18:03:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae20c41e276d25f84fd5e0a38f74416639ad9957a9356c700b28b888f2ed6f4`  
		Last Modified: Wed, 14 Sep 2022 18:03:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f4968981ca0e1cb40d2637aafa6243c345b4511a3769e011db77855b79fab9`  
		Last Modified: Wed, 14 Sep 2022 18:03:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c06a6cf85b2b13b3e04be2018d58cb3e2203e6726503cb8faf75fe0450bbd70`  
		Last Modified: Wed, 14 Sep 2022 18:03:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09521bf391c9276336d29300c051c91eceb62eea17927512648a731fab180a0d`  
		Last Modified: Wed, 14 Sep 2022 18:03:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf2f47b774a286daf220b11f86e03c3497de7f1d43484eb28362cf5bc964f76`  
		Last Modified: Wed, 14 Sep 2022 18:03:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55aea60a6a4f599ce8856a17600e6e3d7aa1bc4d0b000efabe38d623dac9fed`  
		Last Modified: Wed, 14 Sep 2022 18:03:44 GMT  
		Size: 319.9 KB (319898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8538ac0b5b46c7cd2177cad2095fe3363c2ce7c66a4cfa66bc1fa0e269b98c6`  
		Last Modified: Wed, 14 Sep 2022 18:03:43 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
