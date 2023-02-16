## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:07fbc5a89186611e042f7ab23685ae8afbcce5678ff9b1315e742e6935052c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4010; amd64
	-	windows version 10.0.20348.1547; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull caddy@sha256:f78e6d4fc1641b322d4e44adcada628f9acb5106b2e166cbcba796764a4db257
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198e4772b4788d7810819799af107998abe8e241416654ca5406331afefc2908`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:43:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 16 Feb 2023 02:44:00 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 16 Feb 2023 02:45:07 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 16 Feb 2023 02:45:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 16 Feb 2023 02:45:09 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 16 Feb 2023 02:45:10 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Thu, 16 Feb 2023 02:45:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Feb 2023 02:45:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Feb 2023 02:45:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Feb 2023 02:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Feb 2023 02:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Feb 2023 02:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Feb 2023 02:45:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Feb 2023 02:45:17 GMT
EXPOSE 80
# Thu, 16 Feb 2023 02:45:18 GMT
EXPOSE 443
# Thu, 16 Feb 2023 02:45:18 GMT
EXPOSE 443/udp
# Thu, 16 Feb 2023 02:45:19 GMT
EXPOSE 2019
# Thu, 16 Feb 2023 02:46:11 GMT
RUN caddy version
# Thu, 16 Feb 2023 02:46:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f19b532038d3c84c40068e825815f2b252b82869809b11745d9893f12a99ac1`  
		Last Modified: Thu, 16 Feb 2023 02:51:03 GMT  
		Size: 526.3 KB (526332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15f6c8f1e7f194b2b408bf6c4330db67cf7cd4783d39acba2d8384b2f3c31d4`  
		Last Modified: Thu, 16 Feb 2023 02:51:02 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab346a52e8e98a31f0970c85a32f1653b5179dd5ad781a8764b08de792a4d99`  
		Last Modified: Thu, 16 Feb 2023 02:51:05 GMT  
		Size: 14.7 MB (14677251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4451f67396ee792e3ace473ca4a69e5e49639ab8b620e489635a7b2eeb775523`  
		Last Modified: Thu, 16 Feb 2023 02:51:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291ccd53cd67f009cd59c77d90d2623192e5e134fc2ad5a03f1c1860ab66b80`  
		Last Modified: Thu, 16 Feb 2023 02:51:00 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3096247c037e7418f5efc50ce5c7e6bc272ccac5c014f5cb085d77c4c28a3a`  
		Last Modified: Thu, 16 Feb 2023 02:51:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f902038f4ba892bc3e1e4d5fdcef6b7759891c41c067b744fa3d5b008776c90`  
		Last Modified: Thu, 16 Feb 2023 02:51:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82e400c4f2072b1e2b2ff49169de3108075208b544f454b3cdf016be6356321`  
		Last Modified: Thu, 16 Feb 2023 02:51:00 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0944799324319439cbaf2f01dd147e8cc496ea80243ddc22e59e301237acb293`  
		Last Modified: Thu, 16 Feb 2023 02:51:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6c226ffeaa8146cae1b818b43a4776a06f6ce0be460b7d9b42fcc503b39db`  
		Last Modified: Thu, 16 Feb 2023 02:50:58 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0b36e09fd7994e37dd27ccdcfa4610fc1219c4044a95695c6de9f9eecda63b`  
		Last Modified: Thu, 16 Feb 2023 02:50:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f284721a924468c7a0ff80b2809a222ae20cae99d35aa761b5296272783263b`  
		Last Modified: Thu, 16 Feb 2023 02:50:58 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bec609c0b4d99a9726ad86662d32a57664d18dde9d9087c0695ec7e9c4a47c`  
		Last Modified: Thu, 16 Feb 2023 02:50:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ad796550cc1ac21dd77352cf12cc78cacbd0a9f8a1e728e7e4f6a02a0cb9fb`  
		Last Modified: Thu, 16 Feb 2023 02:50:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955699b7dbbfef476622c70f983565943bafe8909c80ec278dff19509fad86`  
		Last Modified: Thu, 16 Feb 2023 02:50:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4096827c6eb36146321a048a5041be746e60afe4c8e90717d681f2d271e0143`  
		Last Modified: Thu, 16 Feb 2023 02:50:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc99e795e3855739a0c170e77263147dec07ac66a9ae51c306705be5af6574b`  
		Last Modified: Thu, 16 Feb 2023 02:50:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8683be90a75d0e97aa8b7002c075e040e7299bd1fde397a541df3e7e4168d97`  
		Last Modified: Thu, 16 Feb 2023 02:50:56 GMT  
		Size: 308.1 KB (308099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156392510131bc65057e3573b9aa9838fccd38cc8ed89734e5255bcd4a315274`  
		Last Modified: Thu, 16 Feb 2023 02:50:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull caddy@sha256:87b9acadc87fc1f78b7ee864f06462a0f45aa263af20fa1744e2f2a0d0870b02
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1695421581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaff43d5343d972f345ff5561ee131879eaafd463e389a1c2607715ac3f6e793`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:46:56 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 16 Feb 2023 02:46:57 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 16 Feb 2023 02:47:25 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 16 Feb 2023 02:47:26 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 16 Feb 2023 02:47:27 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 16 Feb 2023 02:47:28 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Thu, 16 Feb 2023 02:47:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Feb 2023 02:47:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Feb 2023 02:47:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Feb 2023 02:47:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Feb 2023 02:47:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Feb 2023 02:47:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Feb 2023 02:47:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Feb 2023 02:47:35 GMT
EXPOSE 80
# Thu, 16 Feb 2023 02:47:35 GMT
EXPOSE 443
# Thu, 16 Feb 2023 02:47:36 GMT
EXPOSE 443/udp
# Thu, 16 Feb 2023 02:47:37 GMT
EXPOSE 2019
# Thu, 16 Feb 2023 02:47:56 GMT
RUN caddy version
# Thu, 16 Feb 2023 02:47:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961fba6606566986ddd1960cf8309d19fa9deaa486f5a162a60114f3d4c3c82`  
		Last Modified: Thu, 16 Feb 2023 02:51:29 GMT  
		Size: 778.8 KB (778807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af5d76bf41697a16b3336a1857d1e530a3137f28d997c6f5eca0121d42ea88d`  
		Last Modified: Thu, 16 Feb 2023 02:51:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d935f5b810851a2833b69e65d9dcff828f1c6686dab6fa117e9bd08eb95f5990`  
		Last Modified: Thu, 16 Feb 2023 02:51:31 GMT  
		Size: 14.9 MB (14914232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54e2a419181dd9257efde40f9ab80121dd6cc1a478f6ff42d160ddbf5e17cd4`  
		Last Modified: Thu, 16 Feb 2023 02:51:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c07f1bbb0931b3148683baae55ab0d85f8576b2a1d8c2a59bb28544572b5a9d`  
		Last Modified: Thu, 16 Feb 2023 02:51:26 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06073fd741cf5968f24574903b70213f9743b648ebec9c53ccb8fe114ce01ae`  
		Last Modified: Thu, 16 Feb 2023 02:51:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a17243f1184726e21bf0821ee5984a84575b55befba72594fbf0b3a32a47f1`  
		Last Modified: Thu, 16 Feb 2023 02:51:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c403099e0a283f6f2b25b4235c61c8b564a832643f33280253dc040d2a2ab07`  
		Last Modified: Thu, 16 Feb 2023 02:51:26 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc4608f06891b205fbec74e83a221161a2f9d9b50a0b548c3c716d176ee1a4`  
		Last Modified: Thu, 16 Feb 2023 02:51:25 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfe2ac143052b1fa8973567134244ce4ecd1693f16205dd53f0d4cf1b5caa5a`  
		Last Modified: Thu, 16 Feb 2023 02:51:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e217159efeb187bf7ae9a12f6f70764141dd97837f24a517851bc15a36b552`  
		Last Modified: Thu, 16 Feb 2023 02:51:24 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc05a7da758918922e168d1b07b29f4a81d398dc805724dd6b23b4cb28c7b43`  
		Last Modified: Thu, 16 Feb 2023 02:51:24 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832768cea319f33011657944b08b51ea41229fdd7a37f21162dd8aedceb31a6b`  
		Last Modified: Thu, 16 Feb 2023 02:51:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443fc82ac63aefa17f6de497731a007fbc972b175040388a8fda7112834af9fa`  
		Last Modified: Thu, 16 Feb 2023 02:51:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ff50a2c37b226c6e79e3789d1706fc47cb355b14372a147024fc11b2dfb2b`  
		Last Modified: Thu, 16 Feb 2023 02:51:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c6037df6cbd4b9e046dded7157e841a1c40659c4dd082ff9d397c95be6e411`  
		Last Modified: Thu, 16 Feb 2023 02:51:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a470cfe53e2d01e3ca43a7211eb050493a97f430e3c5a52e2364f54a0a4e4834`  
		Last Modified: Thu, 16 Feb 2023 02:51:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d12a1c4350235354af8011d0b2eccb56884eea72a0475197fb007c4fa6c111`  
		Last Modified: Thu, 16 Feb 2023 02:51:22 GMT  
		Size: 359.9 KB (359894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80c894fe52045adaa4c44b9f66422259571c7aec153753d27a56aa3ccbd930`  
		Last Modified: Thu, 16 Feb 2023 02:51:22 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
