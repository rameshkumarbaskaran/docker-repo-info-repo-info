## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bac63d5618da4836e975d70fd7237d2ea16f0db63b1b1b73d81572e960e0154b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:86240b458a2bd0051c3a264220270ce781f78c9b47d5238b77d2a092784c1c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303636391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cdc5b14cd2c15e6a781f2e5cbbfd3b9fb1ad6a2733d8d395a87cedcb36946f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 16:38:20 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 16:41:02 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:41:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Sep 2022 16:41:03 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 16:41:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Sep 2022 16:41:13 GMT
USER ContainerUser
# Wed, 14 Sep 2022 16:41:29 GMT
COPY dir:de893fa6f4d02b385cd95015ab74e60b0c0c67a3785d10d2649390aedc7b2648 in C:\openjdk-17 
# Wed, 14 Sep 2022 16:41:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Sep 2022 16:41:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:07f30e2ceaa03f6ac7b6e6f319083288f48d1fa2a61f36f51f516da241496976`  
		Last Modified: Wed, 14 Sep 2022 16:57:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366e22b303e937ccca7ee1049d6ff7499f528205ccb591a0d932cf3252addc06`  
		Last Modified: Wed, 14 Sep 2022 16:58:59 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e70bf43cde7b760ac8122291c367c2cc47128dd9634074494e86fa7fc37610`  
		Last Modified: Wed, 14 Sep 2022 16:58:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac186b5d9d2033189bf6ee16975920dcc36b8b08058845955f692fc8b9b2ac`  
		Last Modified: Wed, 14 Sep 2022 16:58:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebb961fc182cafd24a1f77bdf2e7fc3ca4d49e28e496c7f2a423955d77eaf3`  
		Last Modified: Wed, 14 Sep 2022 16:58:57 GMT  
		Size: 83.4 KB (83375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3efa23416ae67d7e3cd23faca9709537fbf9ba5914ab51f11f32209e6928418`  
		Last Modified: Wed, 14 Sep 2022 16:58:57 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a26eee7f1246aead0f1c53e27f000f6c5493f30b9644577cb10668c24e535a`  
		Last Modified: Wed, 14 Sep 2022 16:59:17 GMT  
		Size: 185.3 MB (185342897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a1a15bbe85e763d0108d1554aa005cc1c7e68217ba1674fb040972983178cf`  
		Last Modified: Wed, 14 Sep 2022 16:58:57 GMT  
		Size: 72.5 KB (72526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3026b854ce95810cc6043229ee569788a86a3423cfc05cd0bdb2b97f4fae1952`  
		Last Modified: Wed, 14 Sep 2022 16:58:57 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
