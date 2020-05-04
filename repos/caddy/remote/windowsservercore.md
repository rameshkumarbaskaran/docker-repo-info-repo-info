## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:281ddde9309b446b0d11aaffb2736733e315c141a151759baae8a4839d4bb7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64
	-	windows version 10.0.14393.3630; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull caddy@sha256:db85f2c3a6b940fe4607a9c1a6f7e2542c3abbadcc0ab2a1de77b896df142ed3
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288023362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35507000014e161f4e7538b4c6a35c2306b7062c304acda0f6f87281a14311fc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2020 23:15:34 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Mon, 20 Apr 2020 23:35:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 04 May 2020 19:15:12 GMT
ENV CADDY_VERSION=v2.0.0
# Mon, 04 May 2020 19:15:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 04 May 2020 19:15:44 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 04 May 2020 19:15:45 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 04 May 2020 19:15:46 GMT
VOLUME [c:/config]
# Mon, 04 May 2020 19:15:47 GMT
VOLUME [c:/data]
# Mon, 04 May 2020 19:15:48 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Mon, 04 May 2020 19:15:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 May 2020 19:15:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 May 2020 19:15:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 May 2020 19:15:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 May 2020 19:15:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 May 2020 19:15:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 May 2020 19:15:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 May 2020 19:15:55 GMT
EXPOSE 80
# Mon, 04 May 2020 19:15:56 GMT
EXPOSE 443
# Mon, 04 May 2020 19:15:57 GMT
EXPOSE 2019
# Mon, 04 May 2020 19:16:13 GMT
RUN caddy version
# Mon, 04 May 2020 19:16:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9153fe178f6c24d737a32e64b5339d6c98c6f3510991a022194840e79bc4db4f`  
		Last Modified: Mon, 20 Apr 2020 23:21:13 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0181e8dc490f55c1e3f46913e0869af835174a08254258ad3e4927a8337d162`  
		Last Modified: Tue, 21 Apr 2020 00:27:35 GMT  
		Size: 4.7 MB (4701412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091b4fc7a443ca57c3669f083e97df6f84bbb45addc1c1efe6878baa3443385d`  
		Last Modified: Mon, 04 May 2020 19:19:14 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec86d26efce314fd4555822b1656630b56aa67b1527e40ff53252e3ebdfe3656`  
		Last Modified: Mon, 04 May 2020 19:19:17 GMT  
		Size: 12.3 MB (12295601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a616470d4e50bd2f433b61d7ae176161839aa25ffbbf356f19762b42fa996`  
		Last Modified: Mon, 04 May 2020 19:19:13 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16565719ca21e990c11845cc005ec70b15d2d087ebd27ec8e477a032be23ef7`  
		Last Modified: Mon, 04 May 2020 19:19:13 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c62beca22955c09d504f2199d79a4ad16e8292f8b4e2112a344841cbe1019b0`  
		Last Modified: Mon, 04 May 2020 19:19:12 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b622ae76f37c444a65030fcfa69793ccf673fbe136cdc3ef0bd25becf3f8a5a`  
		Last Modified: Mon, 04 May 2020 19:19:12 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27666e5e4bc9209f63bde0a14b6bd54750f163d815346938cc65e339d506b44e`  
		Last Modified: Mon, 04 May 2020 19:19:11 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e0a3b5f7bd06c6cdf9cc0059237db989fb4ecc6f8c7dc7b4da9f418ab31f33`  
		Last Modified: Mon, 04 May 2020 19:19:11 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e330c45416735b6db5abb57bf501516047f1b72f35d9bd5055ac6a5b11ae07ba`  
		Last Modified: Mon, 04 May 2020 19:19:10 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0259f7f6be724e02fa249e94af45a374592117f46bd8830f8bfc18623501fa`  
		Last Modified: Mon, 04 May 2020 19:19:09 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c88a45a3ecff8883ac10fe5f7ce518b4bb764099e98ddb85a624c590736328`  
		Last Modified: Mon, 04 May 2020 19:19:09 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554322af09991a2806922dfb0fccfbb02d4a7a7ef27181b3e3858cef0cfbcf85`  
		Last Modified: Mon, 04 May 2020 19:19:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba619b7348264ab5071bee110c341369c03e4b722fa01c6f610daa523c28abfa`  
		Last Modified: Mon, 04 May 2020 19:19:08 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf821e63cbe00aab351e45af26011be6f8c2a5505a23949ac88cc598c01df38`  
		Last Modified: Mon, 04 May 2020 19:19:08 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc469ac48756707add581a03b6c75856d8ac093f32a4d835016400a940620614`  
		Last Modified: Mon, 04 May 2020 19:19:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dfaf38f5a41db8c57ef8bb820ab11bfab9f652295baf74a1ec89fe594a98eb`  
		Last Modified: Mon, 04 May 2020 19:19:06 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f53adff81fb277cb71da0d3550408bb42b5f6c687d20be45ee243b9da64341`  
		Last Modified: Mon, 04 May 2020 19:19:06 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922f86a02b9b05066bad46178dbaaf5749cbb958466ce42424cf9e92527a1ff`  
		Last Modified: Mon, 04 May 2020 19:19:06 GMT  
		Size: 297.5 KB (297487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f16c5d9ae05feeded180a140af2dc291f996ae32e91c052b9f29d7c062a2b5`  
		Last Modified: Mon, 04 May 2020 19:19:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull caddy@sha256:483811fae53c753c06d339cf61f7e998e844742e2eef2165ca987cf67fa98000
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751078483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1506e8c3a6c7ade7c68c42ef7cb9f7952b56e4bc021edab59815864b7a662ff`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2020 23:17:30 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Mon, 20 Apr 2020 23:35:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 04 May 2020 19:16:25 GMT
ENV CADDY_VERSION=v2.0.0
# Mon, 04 May 2020 19:17:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 04 May 2020 19:17:50 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 04 May 2020 19:17:51 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 04 May 2020 19:17:52 GMT
VOLUME [c:/config]
# Mon, 04 May 2020 19:17:53 GMT
VOLUME [c:/data]
# Mon, 04 May 2020 19:17:54 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Mon, 04 May 2020 19:17:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 May 2020 19:17:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 May 2020 19:17:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 May 2020 19:17:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 May 2020 19:17:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 May 2020 19:17:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 May 2020 19:18:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 May 2020 19:18:01 GMT
EXPOSE 80
# Mon, 04 May 2020 19:18:02 GMT
EXPOSE 443
# Mon, 04 May 2020 19:18:03 GMT
EXPOSE 2019
# Mon, 04 May 2020 19:18:43 GMT
RUN caddy version
# Mon, 04 May 2020 19:18:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ac64d06edc38376c754491fd7ced4aa035af4e675cdc3ac928ea71101af9d`  
		Last Modified: Tue, 21 Apr 2020 00:27:58 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d9ac51d67cd523925abe19d1fefd0f5e5de96dd7f4210eebd601cd07940879`  
		Last Modified: Tue, 21 Apr 2020 00:27:59 GMT  
		Size: 5.4 MB (5407793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381f846c3e0f89bbd6de5263aa83db03bed6d2ea3317625dd372e20169faa780`  
		Last Modified: Mon, 04 May 2020 19:19:38 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3824c79e300c5a9c4d5a19b1f4c818ab2dabfc73204e9f3cf7d94a1b039ee190`  
		Last Modified: Mon, 04 May 2020 19:19:56 GMT  
		Size: 17.3 MB (17320284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b621b926c48a099a7378bd6e59c2ae5f013cfff396c7b99601cc4cd584a9a7`  
		Last Modified: Mon, 04 May 2020 19:19:38 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993ec80086d94e2b010ffc6f03ff399207978dd4ffdd57b81587d660e5b56293`  
		Last Modified: Mon, 04 May 2020 19:19:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1108c387026534722123cc76823fb3657f8fe0f121262da0123ff8b7658cc6f5`  
		Last Modified: Mon, 04 May 2020 19:19:37 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e2c987eb46761454ccd3a2cb0d5b59576b2a868ad2a2e6bf60e65c7da631f4`  
		Last Modified: Mon, 04 May 2020 19:19:36 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8c76842d02c23c931ece6c41bfdb091f483086c711aa385d576388eb7f8eaa`  
		Last Modified: Mon, 04 May 2020 19:19:36 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586957c40d88960ffaea03a011874260112e3cca4211d560a0885ce187141185`  
		Last Modified: Mon, 04 May 2020 19:19:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6b0a8573d2cac0dee10e348b2242058768f5e40b8ac55316770bc574081acb`  
		Last Modified: Mon, 04 May 2020 19:19:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ecf815c04af9e2f6c3830f7b5140aa741be0ccc33d1ffb222cdcfcdc3393ab`  
		Last Modified: Mon, 04 May 2020 19:19:35 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1247f03de6ad47a99acd5cc56f5aca19536903921b33825c7c81ca7c6c5dbf`  
		Last Modified: Mon, 04 May 2020 19:19:33 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65569f34e9fb3189b27094a29a68aea00387b6e47022e16e5ab162d5699cc164`  
		Last Modified: Mon, 04 May 2020 19:19:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f2c1ffbd2829c22e0dc80462e6cfafaf8895c86c882b292f61aa1f9a838fee`  
		Last Modified: Mon, 04 May 2020 19:19:33 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd8c2bdb03f8eee82684e1bd1cab9d7ea01fc8cadd135ed52b1e5e8cd6fe01`  
		Last Modified: Mon, 04 May 2020 19:19:33 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b62857cfcce43061b5da2f2c6f7c946be76b748caa1c28a86d9f95be1cb829`  
		Last Modified: Mon, 04 May 2020 19:19:31 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dde9cce6c5b5a5b317fa9bff6001fa16f962056865b493f6d2739c69c5ec7e5`  
		Last Modified: Mon, 04 May 2020 19:19:31 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25f5b6a1a785c69a3fdfbcdf337268d1a9a931350a7d5e439ae038ac72dd826`  
		Last Modified: Mon, 04 May 2020 19:19:31 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a299406167210c9bfaae272f8c7889b98825781c58fd647b017d29ada40dc6d`  
		Last Modified: Mon, 04 May 2020 19:19:31 GMT  
		Size: 260.9 KB (260946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78cca6bcb21102bbdc672d67917a974c7680d09d056adef5a306bc3c48bb106`  
		Last Modified: Mon, 04 May 2020 19:19:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
