## `adoptopenjdk:11-openj9-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:6ace03a551e863fa41c97d8fd09196d7db6de8ab4c7bbbac7b37629d1e2680f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull adoptopenjdk@sha256:1a39ac831cb9760157dbbe5cda31a35eafa992a14edf5f821b736e661cdb3003
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3023634241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dcca6e016174280d20fd7a91673858d8b8b2aa37446c091d3b4fbb4183b2a1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:30:52 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 09 Jun 2021 18:32:17 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.11_9_openj9-0.26.0.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.11_9_openj9-0.26.0.msi ;     Write-Host ('Verifying sha256 (c4eee9cb72f5abd6ccacfcc565415c424f0f2ae32abca159096995a892ccfe6e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c4eee9cb72f5abd6ccacfcc565415c424f0f2ae32abca159096995a892ccfe6e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:32:20 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 09 Jun 2021 18:32:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ffb642d8df64a93892d9cd5834c7727262b334fdbc996e494d2e7b3831174f`  
		Last Modified: Wed, 09 Jun 2021 19:38:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127f6705b656a0d170a3f63ce8c26fa7252646055b402f07fa7747bcd7fd0fb`  
		Last Modified: Wed, 09 Jun 2021 19:38:38 GMT  
		Size: 382.0 MB (382043484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f99bfdcd314f5e561bc2233c0fb3709ac60b133bbc74cbf0af8680ca63e127`  
		Last Modified: Wed, 09 Jun 2021 19:38:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becf6b6c52b3085f2cd1a571c44a1e1547d2e2c34542c4c390f0545528aab64d`  
		Last Modified: Wed, 09 Jun 2021 19:38:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull adoptopenjdk@sha256:92736ec8703965e0ffe444dfdd3b4f08cc7d78291ef791859270e049ac88ee4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 GB (6652179875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ea06504d5f454ea5a63de1cb3f6247c9baa19a8996bd24776e7602573da4ac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:32:35 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 09 Jun 2021 18:35:11 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.11_9_openj9-0.26.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.11_9_openj9-0.26.0.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (c4eee9cb72f5abd6ccacfcc565415c424f0f2ae32abca159096995a892ccfe6e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c4eee9cb72f5abd6ccacfcc565415c424f0f2ae32abca159096995a892ccfe6e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:35:14 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 09 Jun 2021 18:35:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c82e82e95dbad4ccc260b42e03767eb07222e2f00ec57a69b3c87b17da1d2fd3`  
		Last Modified: Wed, 09 Jun 2021 13:04:25 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fa023f63e9096bf0b4a2f97bcaf66108b27029e3306d2613bc7576a82f40a`  
		Last Modified: Wed, 09 Jun 2021 19:38:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93801a8a6ad9e2caf696c49ca3049833999668eeb80252c5a340f55fe8bc356`  
		Last Modified: Wed, 09 Jun 2021 19:39:25 GMT  
		Size: 386.4 MB (386446956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c36c4e21f053479c6df10c326d5095f68180f75db252aad1870619ffb0fefa`  
		Last Modified: Wed, 09 Jun 2021 19:38:51 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf91e08741ca549bf6ac037aae55f508b071ee10e4c2c9480ae86dbe40bf7721`  
		Last Modified: Wed, 09 Jun 2021 19:38:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
