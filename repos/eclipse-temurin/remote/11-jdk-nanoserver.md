## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b0f6a0c336639c8c63ce849996bf8c6425dfa32381c0bc9d47c2aa59e09fd469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:495df1fc1dc64d65494a978df324164da9f3a28af2bcda41ca3b0fbe87d990d9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309715209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a4a231be309fd3e19ef7c9d055639f429c8fde4b1d19dfb0f03ba91207d92d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 20:19:59 GMT
SHELL [cmd /s /c]
# Thu, 10 Feb 2022 20:28:59 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:29:00 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Feb 2022 20:29:00 GMT
USER ContainerAdministrator
# Thu, 10 Feb 2022 20:29:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Feb 2022 20:29:14 GMT
USER ContainerUser
# Thu, 10 Feb 2022 20:29:48 GMT
COPY dir:9ebff3631ec53abdcb6e4f307c52be82361e65c94c68bdde1fa726e2b087ad3f in C:\openjdk-11 
# Thu, 10 Feb 2022 20:30:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Feb 2022 20:30:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3caa1e550ae326513f81130f539f06a05b30aca3f6ac96039cce37a715c5f008`  
		Last Modified: Thu, 10 Feb 2022 21:15:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee90641fd683fd62c7683c0eeed2f467a3eba23e2fe31fd595f8a1c980d89545`  
		Last Modified: Thu, 10 Feb 2022 21:15:51 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b362a9e00c369a12ed7e8d91ce6fa54248e8bc11ac9834f1debb1c7061e7b0b1`  
		Last Modified: Thu, 10 Feb 2022 21:15:51 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777a63efdac0dbd77fb28e3a91bf1e111cc91082639433992439cf1a2d061e1a`  
		Last Modified: Thu, 10 Feb 2022 21:15:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765baba86fc9ffb96ce8448a6ca1330c02e348a00ebf99927d953d2f726fa658`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 89.3 KB (89255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44abd88b172f82a165ec0247add2c9ac0c56979ed9eefc19a6df6b3bc5434abc`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7419334bbbf031e42ebf1571e5745cfa2900abba7fcb9c28653b7742ba7e462`  
		Last Modified: Thu, 10 Feb 2022 21:19:24 GMT  
		Size: 192.1 MB (192087863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927763b50766543255c3f019c0b89df3a2c01f6e063f33e979c0cbc0cba3d357`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 73.5 KB (73451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb92f281cc0ae9c1b303154e4dd61fea9813b09feeb5bb7c7e840466cd78564`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:0ac50e0c80dd93a7584ba932bc77ff3579c78441e15d95b28e074d51e7c4d6d1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe426282d8d6c317f6bde8c6e2e1540706f9bf45793f754c3d19973d43be5d45`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Thu, 10 Feb 2022 20:22:15 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:22:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Feb 2022 20:22:17 GMT
USER ContainerAdministrator
# Thu, 10 Feb 2022 20:22:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Feb 2022 20:22:33 GMT
USER ContainerUser
# Thu, 10 Feb 2022 20:23:07 GMT
COPY dir:9ebff3631ec53abdcb6e4f307c52be82361e65c94c68bdde1fa726e2b087ad3f in C:\openjdk-11 
# Thu, 10 Feb 2022 20:23:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Feb 2022 20:23:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c012d3b7f4557f22093e79e3988a22ed074a31eb5a9365647e44ee6abb5c43`  
		Last Modified: Thu, 10 Feb 2022 20:47:07 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1310312626f8bd7ad3f88c405eb55492284f16f14ecadea3be9616cacfef6c50`  
		Last Modified: Thu, 10 Feb 2022 20:47:07 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8421e619570fefcfd211fe9d728dedd4e70946e12ba20f3c6580883a836da58`  
		Last Modified: Thu, 10 Feb 2022 20:47:06 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f951f36128cdb26f17d0d4a57c001ef78a30351c1d234786fd7906dc69a2efb0`  
		Last Modified: Thu, 10 Feb 2022 20:47:04 GMT  
		Size: 77.9 KB (77875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0055079e92dbe578c563d705dccb78ac46e37b520edb42b96df7f54a35d23f1b`  
		Last Modified: Thu, 10 Feb 2022 20:47:04 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f444a080193671558faf6723dde431e63dd251d78134239dd2e82fb8978f4f7a`  
		Last Modified: Thu, 10 Feb 2022 20:47:23 GMT  
		Size: 192.1 MB (192104548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c871948be271f9e0d0de3372341a240f1292752601d01bc53b81dcb6cf8edc`  
		Last Modified: Thu, 10 Feb 2022 20:47:04 GMT  
		Size: 89.3 KB (89268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a8cfacc61b92ed43dd0203d5b7be7487236630e5dda8f2b317fe7a270cbadb`  
		Last Modified: Thu, 10 Feb 2022 20:47:04 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
