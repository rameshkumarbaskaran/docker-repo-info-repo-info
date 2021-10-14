## `eclipse-temurin:17_35-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:576798b21926c01e42f33ab86ef021208e020f8181edc70f632fe1d94babb06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:17_35-jdk-nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:0d9120c5b1318669336f10c6dd798417410ee29b7db448806940f96a52a9e987
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302060962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8b9f9d6c399d06f04db1228c66c0d84a1817d2459ae2df350607167d99df7b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 19:05:36 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 13 Oct 2021 19:05:37 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Oct 2021 19:05:38 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 19:05:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 19:05:52 GMT
USER ContainerUser
# Wed, 13 Oct 2021 19:06:09 GMT
COPY dir:ba92fda3ecc57988e3fdb5e98847d06c9e695148297ce16b53bb487a02cbd557 in C:\openjdk-17 
# Wed, 13 Oct 2021 19:06:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Oct 2021 19:06:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c661f0d3ec9066fc9744b0c9526a413a9ba4a0850fe2a13538f1fc15338008af`  
		Last Modified: Wed, 13 Oct 2021 19:45:58 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b475be6d1811669871d5e53fd2cb23b4b24b7e56e7bbd9a99f5fb887fc0893d2`  
		Last Modified: Wed, 13 Oct 2021 19:45:58 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd627f227d2263c5cb99f5e46aa8cff0fae5b6693eebd140181800fcaf020b2`  
		Last Modified: Wed, 13 Oct 2021 19:45:58 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aec7e9045f1d17fb7aefe3e73578eff8fe3bce3a3b8a8e4ec5c7e82296a4b21`  
		Last Modified: Wed, 13 Oct 2021 19:45:56 GMT  
		Size: 88.3 KB (88336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642601194ae14b5bf34961541dd8fd94ea2155c3fbc01d21db9e8098c00b2ce0`  
		Last Modified: Wed, 13 Oct 2021 19:45:56 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff0d13d234c5ab43f578e7b7df3bfa5da6d64a83bb3cf79b9f7763bd4f18468`  
		Last Modified: Wed, 13 Oct 2021 19:46:16 GMT  
		Size: 184.9 MB (184940017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e180e64c7a71ba9add366cb312af206a44f340d48eb57c6d2b09b188d90e8da`  
		Last Modified: Wed, 13 Oct 2021 19:45:56 GMT  
		Size: 86.2 KB (86245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513bf6dbabda4c2c5886107050e06c23cf5f5e47ed4d2249252e09ab4f63b1c8`  
		Last Modified: Wed, 13 Oct 2021 19:45:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17_35-jdk-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:db3665d01311fa3a7f8d1cb76398a8469d230af2bf2dca6e4f02325d0fe810d7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291286956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8398ff069ede7a81941acc232b4d1a87063ff6f96c5097b1773422845d5b0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 18:58:00 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 13 Oct 2021 18:58:01 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Oct 2021 18:58:02 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 18:58:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 18:58:17 GMT
USER ContainerUser
# Wed, 13 Oct 2021 18:58:34 GMT
COPY dir:ba92fda3ecc57988e3fdb5e98847d06c9e695148297ce16b53bb487a02cbd557 in C:\openjdk-17 
# Wed, 13 Oct 2021 18:58:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Oct 2021 18:58:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca57c0d4ceadd14c4d4f4c4d6e06fda712d25c8e85a69fad2208edd397d638b9`  
		Last Modified: Wed, 13 Oct 2021 19:42:40 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e758083b008ffafc69eb903f8054026b79131442a66146c0a92363729584d`  
		Last Modified: Wed, 13 Oct 2021 19:42:40 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e86d7dcefed0131f0cdbf638a82a8fdccf6f89db2c11ead18c0951722c975a4`  
		Last Modified: Wed, 13 Oct 2021 19:42:40 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2a1c65502e3d6a07b259e3bc7a7e69c26bf927d7ef0db99800c044dd78ab1e`  
		Last Modified: Wed, 13 Oct 2021 19:42:37 GMT  
		Size: 71.7 KB (71747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1681ad519dae7b4002fa42110113243e8c2f1ef246882a2c67e430d4bcf0c1d`  
		Last Modified: Wed, 13 Oct 2021 19:42:37 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb0612b4ca3019298927a2e321d0f61ee40e96f3112d05893b7ebe5ff2266a0`  
		Last Modified: Wed, 13 Oct 2021 19:42:57 GMT  
		Size: 184.9 MB (184936637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341ed370660b49ebadeb550967ed077347c429d6cc465d73f1ddb3fa913fc4e4`  
		Last Modified: Wed, 13 Oct 2021 19:42:43 GMT  
		Size: 3.6 MB (3610481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97068abf3f9a2d5b19b763c9dab191e2db2fb992f1e4446aba8f5b5781ff02f3`  
		Last Modified: Wed, 13 Oct 2021 19:42:37 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
