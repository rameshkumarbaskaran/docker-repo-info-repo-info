## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:9c8a1111568a30c4af385e4f2ab85cafe978a489eb71f1015fa3cca615b49a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.3046; amd64
	-	windows version 10.0.20348.768; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.3046; amd64

```console
$ docker pull caddy@sha256:e098b2a13a45d9eac489cfaf3c1650eeb428271fcf8755155ec743ada620a41f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2677963935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c28dcb1867f001cdaa206724c76456253bf29b8f32cfe4104e901a72fa1e62`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 20:48:07 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jun 2022 20:48:08 GMT
ENV CADDY_VERSION=v2.5.1
# Wed, 15 Jun 2022 20:49:23 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.1/caddy_2.5.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4294796c4bd4bed0c593d83606a5413de30f35f88d624e1b1e5b6cd8672ffbcc7a689d7ce4ef30c1abea0e95eda62220faac15d2a6aca0c3e2b418abe7a74118')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jun 2022 20:49:24 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jun 2022 20:49:25 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jun 2022 20:49:27 GMT
LABEL org.opencontainers.image.version=v2.5.1
# Wed, 15 Jun 2022 20:49:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jun 2022 20:49:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jun 2022 20:49:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jun 2022 20:49:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jun 2022 20:49:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jun 2022 20:49:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jun 2022 20:49:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jun 2022 20:49:35 GMT
EXPOSE 80
# Wed, 15 Jun 2022 20:49:36 GMT
EXPOSE 443
# Wed, 15 Jun 2022 20:49:38 GMT
EXPOSE 2019
# Wed, 15 Jun 2022 20:50:29 GMT
RUN caddy version
# Wed, 15 Jun 2022 20:50:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ecf983527a47c575916bff83b7fe3bffe5b5d3ebbda5f6e0b3886f41238f55`  
		Last Modified: Wed, 15 Jun 2022 20:55:08 GMT  
		Size: 363.6 KB (363648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e03101e321792db16dd6c8237b418b61e5dfde3543226d285f9a3c263db428`  
		Last Modified: Wed, 15 Jun 2022 20:55:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6025f63ee42899e10196434f91fcb8759a669d1d0fb937803bc5ac8547ee2d`  
		Last Modified: Wed, 15 Jun 2022 20:55:23 GMT  
		Size: 14.0 MB (14006419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc2c31508537cb7dd58f543a2d118da82568b3184b1cca8d5f4a6fba13dd755`  
		Last Modified: Wed, 15 Jun 2022 20:55:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b333678c68556a8c9aa3e959a8bace2d463f2daa9e95315c8d49aba730dc6c`  
		Last Modified: Wed, 15 Jun 2022 20:55:06 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d7308f5d665bd0fdf426d843f8ccd81638bfee0795f3882d2c50f185bd7a3d`  
		Last Modified: Wed, 15 Jun 2022 20:55:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a6d7a6d31923518edd902c5b922437302adc4bdf43493adfcd957234073b5f`  
		Last Modified: Wed, 15 Jun 2022 20:55:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e91e80302901fff17a73dfb4a0ce5192ceb4acd1df2bf12a73c1b8f723865a`  
		Last Modified: Wed, 15 Jun 2022 20:55:05 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da64de3dc209d51a8c6eecf42a0ca61db4c4b0a7b956339484a3216588fcaa7d`  
		Last Modified: Wed, 15 Jun 2022 20:55:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00548178d25aa1c28b9675471b8721a86d17b42f1a580b3d9009ba02d37c7d3`  
		Last Modified: Wed, 15 Jun 2022 20:55:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2a96801039ff1b305a61140ed47e1a11959d23fef958bd740be1c80f7d9fcc`  
		Last Modified: Wed, 15 Jun 2022 20:55:03 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109e5f802b58cf6af4615662230fde9cfed73918e6e99dda390132a6e5abf637`  
		Last Modified: Wed, 15 Jun 2022 20:55:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e0ee72a29dd629fa2339914e15593a002f687d767d3df9a24c4d06799bbe4d`  
		Last Modified: Wed, 15 Jun 2022 20:55:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ff80ebe2c401a9da2622bbe7f9a26377208e1c910b9e5bdf9b4c564ae5c9b`  
		Last Modified: Wed, 15 Jun 2022 20:55:01 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8847c4342cd433d6bfb6bfe8d1a2bc401828e23f95829ad3c14f59ff3f89b27c`  
		Last Modified: Wed, 15 Jun 2022 20:55:01 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c533dfceaaa344b42325107a50f33ccd68662594753a3ac9ff58af418901f1c8`  
		Last Modified: Wed, 15 Jun 2022 20:55:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e75df73d93d481a3daca5a7669d87e220242fbb9e7ab567d99e9ecd49fb141c`  
		Last Modified: Wed, 15 Jun 2022 20:55:01 GMT  
		Size: 291.3 KB (291330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1113eef21412abb758c12021ce14119182fe5fe0a9284fba5174b810ce3ade`  
		Last Modified: Wed, 15 Jun 2022 20:55:01 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.768; amd64

```console
$ docker pull caddy@sha256:ce3ae82aedf7b09f0296ee640d436be64ac848c479c10b9a4e68c75b856ea151
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2293726019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80827f5a91067b64691dff8dd32638fc2f2a19a24d4cd0c06faab0c40431050b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 20:51:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jun 2022 20:51:09 GMT
ENV CADDY_VERSION=v2.5.1
# Wed, 15 Jun 2022 20:51:36 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.1/caddy_2.5.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4294796c4bd4bed0c593d83606a5413de30f35f88d624e1b1e5b6cd8672ffbcc7a689d7ce4ef30c1abea0e95eda62220faac15d2a6aca0c3e2b418abe7a74118')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jun 2022 20:51:37 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jun 2022 20:51:38 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jun 2022 20:51:39 GMT
LABEL org.opencontainers.image.version=v2.5.1
# Wed, 15 Jun 2022 20:51:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jun 2022 20:51:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jun 2022 20:51:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jun 2022 20:51:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jun 2022 20:51:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jun 2022 20:51:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jun 2022 20:51:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jun 2022 20:51:48 GMT
EXPOSE 80
# Wed, 15 Jun 2022 20:51:49 GMT
EXPOSE 443
# Wed, 15 Jun 2022 20:51:50 GMT
EXPOSE 2019
# Wed, 15 Jun 2022 20:52:07 GMT
RUN caddy version
# Wed, 15 Jun 2022 20:52:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5532718205dc0ed50a39a6595b5765be686bb59ab201ba3ad42ae6690834a390`  
		Last Modified: Wed, 15 Jun 2022 20:55:46 GMT  
		Size: 640.7 KB (640676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cbbcdd20c61bc49f442d2fa1561992b98b35c6d96170a0b9c9f268f893049`  
		Last Modified: Wed, 15 Jun 2022 20:55:45 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4a6cc2b805dda4b989b3a84618f89687d821f4d4b8d9de9b8727f50a4f453a`  
		Last Modified: Wed, 15 Jun 2022 20:55:59 GMT  
		Size: 14.2 MB (14247883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b3c43bd0e7a747300fa38d10d5b0a65ae929a5c4471d87748540331fe29a2`  
		Last Modified: Wed, 15 Jun 2022 20:55:43 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f4b8bcdb9b73faabf9ab92336e96de48b846c65926d9271a37a0c6ccf96d66`  
		Last Modified: Wed, 15 Jun 2022 20:55:43 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b08720d1b524e40438b834954518796fb3064acb80c18bf405420e515de83`  
		Last Modified: Wed, 15 Jun 2022 20:55:43 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3e8049043777fa7beb99a2d7d9f4ece307fae9b741fe12c4942b0e852b4102`  
		Last Modified: Wed, 15 Jun 2022 20:55:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2369ca53e4ffe697142d4fabdff170b754db13838d60b3690f26e0cbfda1cdb`  
		Last Modified: Wed, 15 Jun 2022 20:55:42 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2561c0217363428ad75bbe4776344a00566543c2393a28ee12eddae5c497561`  
		Last Modified: Wed, 15 Jun 2022 20:55:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f1525f5ca8e9f365fb533c66f1c22660c59c954cd10e0304a162a1b4b62522`  
		Last Modified: Wed, 15 Jun 2022 20:55:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c89e100cac643ea136f41d80f225decf34302813d569848824d789b7732c80`  
		Last Modified: Wed, 15 Jun 2022 20:55:40 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2395e1df6b4b034a0dce23e4102df2657365b54136bdf504de2cab157f07db1`  
		Last Modified: Wed, 15 Jun 2022 20:55:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7bec90e6bec361afca7861a9a9a63e8572879d5955f1fe9f5e2fefad254da0`  
		Last Modified: Wed, 15 Jun 2022 20:55:40 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f14acd665aef8bd887ebff4ff255708f6e82b8fdb8347067d73218d5c13eba`  
		Last Modified: Wed, 15 Jun 2022 20:55:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf15909eb638b723079bfbb5e65ec051222280895a3ef02eb688095f12e452d`  
		Last Modified: Wed, 15 Jun 2022 20:55:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f469a5cf263f04fc72b356ed5c0d13fac36a71d5212b405059e7d6833d67bb`  
		Last Modified: Wed, 15 Jun 2022 20:55:38 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f16c21f8fb8fd90ce75cee713252d2b585349562fe7a0678a5225fe3f98cfb`  
		Last Modified: Wed, 15 Jun 2022 20:55:38 GMT  
		Size: 350.6 KB (350618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21e7db6b1803a2939df33237467c402a1f0521923e0e0a1c9ab998f04219db2`  
		Last Modified: Wed, 15 Jun 2022 20:55:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
