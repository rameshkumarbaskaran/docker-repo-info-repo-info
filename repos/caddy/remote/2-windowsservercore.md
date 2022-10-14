## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:a2ab9b4da81fb5793c09308f6353dec3d5aa70255288aa5a9390cf5333e74935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.3532; amd64
	-	windows version 10.0.20348.1129; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull caddy@sha256:c795b26fccceaa3ea3738c3d086e0c9da9978392aeb6e2c69ae3d71131b88998
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726785951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0ffc50daa8e99f5d3029bd930601ec939b66a180da1ad5fef783d1fcb69eb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 16:58:31 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/8c5fc6fc265c5d8557f17a18b778c398a2c6f27b/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/8c5fc6fc265c5d8557f17a18b778c398a2c6f27b/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 13 Oct 2022 23:14:49 GMT
ENV CADDY_VERSION=v2.6.2
# Thu, 13 Oct 2022 23:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.2/caddy_2.6.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('1454eb2de857fa091a00e62199bb5ea7840210a90a9b04f626f0cf3688cdf69ea736b497e3b8ac0f1b40bb9aba416bfa9e4eb9c33be166665ee0ce02a26cfd98')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 13 Oct 2022 23:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 13 Oct 2022 23:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 13 Oct 2022 23:16:12 GMT
LABEL org.opencontainers.image.version=v2.6.2
# Thu, 13 Oct 2022 23:16:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 13 Oct 2022 23:16:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 13 Oct 2022 23:16:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 13 Oct 2022 23:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 13 Oct 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 13 Oct 2022 23:16:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 13 Oct 2022 23:16:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 13 Oct 2022 23:16:19 GMT
EXPOSE 80
# Thu, 13 Oct 2022 23:16:20 GMT
EXPOSE 443
# Thu, 13 Oct 2022 23:16:21 GMT
EXPOSE 443/udp
# Thu, 13 Oct 2022 23:16:22 GMT
EXPOSE 2019
# Thu, 13 Oct 2022 23:17:16 GMT
RUN caddy version
# Thu, 13 Oct 2022 23:17:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77462c8fbd8b2782ee2fc5f09bebfb350912f754186b058478ab8d22f50bb047`  
		Last Modified: Wed, 12 Oct 2022 17:04:34 GMT  
		Size: 358.2 KB (358248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a372be4d9f43d4d5884bc4093c44aedf12150f55ea9457baa2fcceb43ef8074`  
		Last Modified: Thu, 13 Oct 2022 23:21:08 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a8993c29bb6d4c31b0be3609bc7fb2af2666435fe70bb2f329784277d629d1`  
		Last Modified: Thu, 13 Oct 2022 23:21:11 GMT  
		Size: 14.9 MB (14947938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98662b730099437011356fa77ef9072054f4ad73d3781e9b02d4750689762162`  
		Last Modified: Thu, 13 Oct 2022 23:21:07 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7e77f6a080ad6fa8a7320831868ccd7b6385e995988f2e6cca76090a565c99`  
		Last Modified: Thu, 13 Oct 2022 23:21:06 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec71d29d036cab0bdbc7765216513aad527933ededfec4492a97724c6bab52d`  
		Last Modified: Thu, 13 Oct 2022 23:21:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a11bac4631094c366303dd3c571fe04cf1b543bafba72d8dd1030f8ae2ec185`  
		Last Modified: Thu, 13 Oct 2022 23:21:05 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4dc588cdabd0672f8b29c59cd9ddc6d927160284a6f6529fbe39b8e34ca766`  
		Last Modified: Thu, 13 Oct 2022 23:21:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f39777f21d48153f681f16b5a1cd2e12440066bc96a665fa3b85a6275b74942`  
		Last Modified: Thu, 13 Oct 2022 23:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638736df2ba6ceaed21b97ee12046d2d0494561bd735581618ab505ff602b0da`  
		Last Modified: Thu, 13 Oct 2022 23:21:04 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0fe53dba785fdf61d7431392d7e15beeebbe5f215d9a2de2ee00975e7b5c4`  
		Last Modified: Thu, 13 Oct 2022 23:21:03 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fb7b8fc42485b0656b2afcb99344cda044ce10d0107cc91955fbe11433c358`  
		Last Modified: Thu, 13 Oct 2022 23:21:03 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb8f166931be4f8f0b0a07611df01a8e7d1101f8a8ce564144ded43917e1021`  
		Last Modified: Thu, 13 Oct 2022 23:21:03 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bc6f4b7a114b7722cfc81aa83b74727261766c2cef9bc0787e447435c33d2a`  
		Last Modified: Thu, 13 Oct 2022 23:21:03 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5563ab3963680a40da3bc2269bbc1e76362b359547dae9705892cf8f54b50dd1`  
		Last Modified: Thu, 13 Oct 2022 23:21:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d300f0320cd2b8ce3f3e58cbb3acb06e24c5f59a342725056a10667329f914`  
		Last Modified: Thu, 13 Oct 2022 23:21:01 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfb9dfa0b00914a255876439613219f4a74e83734df6b8a197e6e0bb53bf905`  
		Last Modified: Thu, 13 Oct 2022 23:21:01 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b9233dbf203ca77eea2271813856d219ba7d2f633adf99f3262612edfad738`  
		Last Modified: Thu, 13 Oct 2022 23:21:01 GMT  
		Size: 291.8 KB (291836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefde31b509f056641749adae4daa4e0ad3265d260ac1c61b41c8950a10824e6`  
		Last Modified: Thu, 13 Oct 2022 23:21:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull caddy@sha256:e1e15c80e157d71221ec43035cae93b3ea8ba7a6b203428e93159aa6ff5e1463
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432333411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbd806ca24dfacee0d098f111cc9f6d5f42fdbd9db91a63a8de0d048d3984d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 17:01:07 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/8c5fc6fc265c5d8557f17a18b778c398a2c6f27b/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/8c5fc6fc265c5d8557f17a18b778c398a2c6f27b/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 13 Oct 2022 23:17:37 GMT
ENV CADDY_VERSION=v2.6.2
# Thu, 13 Oct 2022 23:18:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.2/caddy_2.6.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('1454eb2de857fa091a00e62199bb5ea7840210a90a9b04f626f0cf3688cdf69ea736b497e3b8ac0f1b40bb9aba416bfa9e4eb9c33be166665ee0ce02a26cfd98')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 13 Oct 2022 23:18:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 13 Oct 2022 23:18:13 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 13 Oct 2022 23:18:13 GMT
LABEL org.opencontainers.image.version=v2.6.2
# Thu, 13 Oct 2022 23:18:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 13 Oct 2022 23:18:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 13 Oct 2022 23:18:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 13 Oct 2022 23:18:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 13 Oct 2022 23:18:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 13 Oct 2022 23:18:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 13 Oct 2022 23:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 13 Oct 2022 23:18:21 GMT
EXPOSE 80
# Thu, 13 Oct 2022 23:18:22 GMT
EXPOSE 443
# Thu, 13 Oct 2022 23:18:23 GMT
EXPOSE 443/udp
# Thu, 13 Oct 2022 23:18:24 GMT
EXPOSE 2019
# Thu, 13 Oct 2022 23:18:40 GMT
RUN caddy version
# Thu, 13 Oct 2022 23:18:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cd84a277fd91a008fe0c8fc7d6706544075a294512940b16f57998588ea892`  
		Last Modified: Wed, 12 Oct 2022 17:04:58 GMT  
		Size: 616.9 KB (616893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94b069dfbedeca0437916f85fdd78a598955839b91ffc4cba4d6327e5c79487`  
		Last Modified: Thu, 13 Oct 2022 23:21:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5263d846656ffa3662062b1a58d9c6d114e00fa5344edc9b93ea5895c4fa46`  
		Last Modified: Thu, 13 Oct 2022 23:21:34 GMT  
		Size: 15.1 MB (15149356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e378404d94c7fb280c51201d60aef05af3196a0ead3b716521cedbe766ba5e3e`  
		Last Modified: Thu, 13 Oct 2022 23:21:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11749bcf2c3e4097f9a1a30d1fc22184e48c94ab54945730c51c36be175c668d`  
		Last Modified: Thu, 13 Oct 2022 23:21:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb14f39fa0dce5d6dab4bdd1a896c02b5a6bba01dcd46ed36928c2cce27295`  
		Last Modified: Thu, 13 Oct 2022 23:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf622a21cfc36d8958be2f273f52b7d4824d500be08f6a2de791506dcc6c981f`  
		Last Modified: Thu, 13 Oct 2022 23:21:29 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b246af35953d05f1c4292cb1cf8cfc29215ceac2e013ae2a0759aa2d216516`  
		Last Modified: Thu, 13 Oct 2022 23:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08367cd2562c20737156e692dca481f835f4832fabb63602fb5edc78494057ae`  
		Last Modified: Thu, 13 Oct 2022 23:21:29 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6d70510bf329eff739580f04b59acba9cb4aa74e57bcb6fca996d6df6b6d2c`  
		Last Modified: Thu, 13 Oct 2022 23:21:27 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc6e963fa5949ceb99519a652299dea21a92c9389aadabedb2deeb4e51855b5`  
		Last Modified: Thu, 13 Oct 2022 23:21:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d175d8244325a62c683c4d1fa6cc266f73231f93142fd0f52c3378da6db1464`  
		Last Modified: Thu, 13 Oct 2022 23:21:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4ce9495075c9b00994ef154c9eb0974ba1853a8244869e35af4eecfca4dce7`  
		Last Modified: Thu, 13 Oct 2022 23:21:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ceee07aab1c573de692984f7655da9e6c4aee31260b8df8735344242e6f1ff8`  
		Last Modified: Thu, 13 Oct 2022 23:21:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295041dd24e85177aaf7e1bbd1c0b032d2eafaf3da59213972894238dd5b3d72`  
		Last Modified: Thu, 13 Oct 2022 23:21:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3583f031f13dfd9a933b6e8d4808a3ac7f3e007d2e751af9581b76b08b6e0c4a`  
		Last Modified: Thu, 13 Oct 2022 23:21:25 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603973d06c7b0a01ab165d727b40f842361ce898a8e7b8579d6bd9db938c8a6`  
		Last Modified: Thu, 13 Oct 2022 23:21:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c4bf5f410b0a58ef5b477fdf99b90ad01e7deb85b685cf06eaae5c9d83a531`  
		Last Modified: Thu, 13 Oct 2022 23:21:25 GMT  
		Size: 319.8 KB (319842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da4c854489e4317220200f8dca47e2335696fe8fa9e7a2aa678467b12b4db7b`  
		Last Modified: Thu, 13 Oct 2022 23:21:25 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
