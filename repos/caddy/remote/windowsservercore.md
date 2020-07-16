## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:c69acf82737ac04895de0fe82b6460bf07cbb49ba46a3b50df15e1210d7630bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
