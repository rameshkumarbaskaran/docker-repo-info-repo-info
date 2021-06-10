## `adoptopenjdk:11-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:85fa0b28b5a33392f661a48cc643e33551320c6dd7338410bd89fd054cd309f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `adoptopenjdk:11-hotspot-windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull adoptopenjdk@sha256:4d548c9793c23abc188202e62abc189d84bb17f6c166b82c7ee84c9b450c394e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3006015472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162b023685377b4d6249aa9e6cee6843c32e30a02b80e7b3b75c80228d35e479`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:01:41 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Wed, 09 Jun 2021 18:03:03 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.11_9.msi ;     Write-Host ('Verifying sha256 (de7de70fbd9f3ff49ce34db87c5f331a5c0b72e54c16e9e6d9ba3007d23b361e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'de7de70fbd9f3ff49ce34db87c5f331a5c0b72e54c16e9e6d9ba3007d23b361e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:03:06 GMT
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
	-	`sha256:df0dd76638fc06d0475a891090d106195abdabd342df755f585bf3c290801a46`  
		Last Modified: Wed, 09 Jun 2021 19:07:57 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d955b8809f57720c22ef72c94f20abb68ec12cfe0f36a3cc39d6c11084c817`  
		Last Modified: Wed, 09 Jun 2021 19:15:19 GMT  
		Size: 364.4 MB (364426126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dd7e0cae084800b97362226483e3549aa850f47f6e5f6d367c82ee21a2e449`  
		Last Modified: Wed, 09 Jun 2021 19:07:57 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-hotspot-windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull adoptopenjdk@sha256:89f12386a1fbd9db973e4ca1b27e86f3ca7edcdbc5b07b6969c92d1e35f48450
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6630099212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8baabfaa409da211be46f4078d7cd044618c1e5d73247c9007288bf29112749c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:03:23 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Wed, 09 Jun 2021 18:05:47 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.11_9.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.11_9.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (de7de70fbd9f3ff49ce34db87c5f331a5c0b72e54c16e9e6d9ba3007d23b361e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'de7de70fbd9f3ff49ce34db87c5f331a5c0b72e54c16e9e6d9ba3007d23b361e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:05:50 GMT
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
	-	`sha256:18b1a684d421e6462e9b56c74ea1e4e3d1e1bb3d2b38a30ae10c12186b42a351`  
		Last Modified: Wed, 09 Jun 2021 19:15:37 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee56dba8ff900240d786c829855845576fdbe8fc10f0907ffc3b432a42ef63c`  
		Last Modified: Wed, 09 Jun 2021 19:16:09 GMT  
		Size: 364.4 MB (364367664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea7c0a325668418e163ba28add982e133f213f53ce54ec8a84b6a09fc520463`  
		Last Modified: Wed, 09 Jun 2021 19:15:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
