## `openjdk:20-ea-7-jdk`

```console
$ docker pull openjdk@sha256:48b71d82bf36b37dfd6e698a84be3abe1bee96debaa8a17d9fc6b3a7eadeed4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `openjdk:20-ea-7-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:873e2456fbaef709adedb51589ff3799e1ba5825e921ad87da8c646b37f97ad7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249768626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36447b523a6b4f31c1db08afe928442b53a2989f31fc5fb95d50c1989cce4376`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:49:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:49:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 22:49:44 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 22:49:44 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:20:40 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:21:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:21:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e62647f09f0ab1a3ac2d84823777bead33aa8e201c13b86c063296e8268023`  
		Last Modified: Tue, 05 Jul 2022 22:58:01 GMT  
		Size: 13.5 MB (13505357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f686e62675201bb118541a9e816e985b783624aba87cbf7ab2f374ea70e87`  
		Last Modified: Thu, 21 Jul 2022 23:30:13 GMT  
		Size: 197.0 MB (197041148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-7-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7058dfc5bd6c646f4d3910ebf4830764e5f2e4b86af52539bf342db7c06e9a83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248198342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4540f84042a7cce58893601fb72a1ed0a3ba0eec765be3c8ec389428b93afb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:04:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:04:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 23:04:02 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:04:03 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:40:38 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:40:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:40:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c622a5406eea6948259fe9d62dd3f3f40ef71254cb260355242ef51e23880970`  
		Last Modified: Tue, 05 Jul 2022 23:20:55 GMT  
		Size: 14.3 MB (14282866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6494d0350bebe5e159625bec2298d2e97b8dbeae5fb3a503a3eba9315e30b2`  
		Last Modified: Thu, 21 Jul 2022 23:56:30 GMT  
		Size: 195.9 MB (195887719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-7-jdk` - windows version 10.0.20348.825; amd64

```console
$ docker pull openjdk@sha256:4171d3540eda4be9eec55a5767446da86c564bc875aad25379f034c6b2454020
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2494234143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcf399a0171b96dd9e589ed99b629e5bed2add9ae4edd5e819240d371c4dd8e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 15:47:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Jul 2022 15:47:48 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Jul 2022 15:48:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 21 Jul 2022 23:14:59 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:15:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_windows-x64_bin.zip
# Thu, 21 Jul 2022 23:15:00 GMT
ENV JAVA_SHA256=9a7a89b8dfa1e693242e7571b791918e37756ebd78e4541d09c6341ea8afe612
# Thu, 21 Jul 2022 23:15:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 21 Jul 2022 23:16:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6a9bb0f902c90ab99dd7b3c8634f73649b052868aa5272230088be93b0be1f`  
		Last Modified: Mon, 18 Jul 2022 21:21:07 GMT  
		Size: 655.6 KB (655645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e59550359c0c386380ad4578a16e628937ecdcba2d6ade5b85605f16407fd`  
		Last Modified: Mon, 18 Jul 2022 21:21:06 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa1e5a40ba69746aa5696dc0a07d417cd9201faa86690739a86198d3a7a9b91`  
		Last Modified: Mon, 18 Jul 2022 21:21:06 GMT  
		Size: 555.8 KB (555764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d40c1bb3b93d05953fbec2b0556557eadba9ce01838bf4edf3c34f8687c034`  
		Last Modified: Thu, 21 Jul 2022 23:26:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c78829108e94292f239900fb5476d8f2ad330cd6ffd404c0c41cd1216dfb65`  
		Last Modified: Thu, 21 Jul 2022 23:26:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b53e84169a3dc54bc806ce262bef675d9b7f84362f7446c52f80f1e906f6f40`  
		Last Modified: Thu, 21 Jul 2022 23:26:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0835a2cd33adcf90c8e7d76515a0bab963f7d67e28b71f3556e68e7801b5cc22`  
		Last Modified: Thu, 21 Jul 2022 23:27:13 GMT  
		Size: 192.8 MB (192783202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fe256f05ca24bb31cca5fd7017a8a7e7dae7d6afec1dcfa87e015464a4ecd`  
		Last Modified: Thu, 21 Jul 2022 23:26:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-7-jdk` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:dca29582ee5917a1be2494715f29e563d95476b2a6cf32789a25b9d16c4aa8bd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2865296583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5be5c00ee532ad4de56734abf126b2923e0475d0e752de931948ad87305de5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 15:50:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Jul 2022 15:50:05 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Jul 2022 15:50:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 21 Jul 2022 23:16:12 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:16:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_windows-x64_bin.zip
# Thu, 21 Jul 2022 23:16:14 GMT
ENV JAVA_SHA256=9a7a89b8dfa1e693242e7571b791918e37756ebd78e4541d09c6341ea8afe612
# Thu, 21 Jul 2022 23:17:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 21 Jul 2022 23:17:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acf5949ddc551d281d19646d7dbeb4f3772073cf86c194f6d98c8afe422f3b5`  
		Last Modified: Mon, 18 Jul 2022 21:21:50 GMT  
		Size: 353.5 KB (353532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ca4f44b32042d608ce9b62563bbff47ca623a4ca4ca22575a680b990a1d675`  
		Last Modified: Mon, 18 Jul 2022 21:21:50 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4525c6bc4913f609856004e14ff912919aa9219c0df562367a0764e7ae034f5`  
		Last Modified: Mon, 18 Jul 2022 21:21:50 GMT  
		Size: 311.6 KB (311646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcacf3f270070af41bd7cdbc141fb0f833c45c213e0fa18edd7a789e3ffa4e1`  
		Last Modified: Thu, 21 Jul 2022 23:27:34 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5ccc329e0ed5d9e0ceab4641be619be735c27fc40c6cdb2b2dde8363c0f257`  
		Last Modified: Thu, 21 Jul 2022 23:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb9f19a8a90583825fb47eb0d17b1e50e1f41d4eece4bb3cf20bd38036e8a17`  
		Last Modified: Thu, 21 Jul 2022 23:27:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d6ed9ac29623140a647f6ec845a48e138439cc3a5a3f9e0536fadf4653c0f`  
		Last Modified: Thu, 21 Jul 2022 23:27:58 GMT  
		Size: 192.6 MB (192579574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e002e25e41e0ba55f7652314228b4e8ab54f712e62c463333654d5f51fcf1f`  
		Last Modified: Thu, 21 Jul 2022 23:27:35 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
