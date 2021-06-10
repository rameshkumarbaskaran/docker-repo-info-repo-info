## `adoptopenjdk:8u292-b10-jdk-openj9-0.26.0-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:00d98b9f34c5854e5bde140474a369cf75f7ee7a1c589e5c6ff099cd32b94e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `adoptopenjdk:8u292-b10-jdk-openj9-0.26.0-windowsservercore` - windows version 10.0.17763.1999; amd64

```console
$ docker pull adoptopenjdk@sha256:77b637d58895661ce596d6b60dbfcf850bc31dffc8833b101f7235f277003709
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2860970677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3a22d2fc84f3011d76c3e662ba37fa82d504e88a1c83e2776c74a95eb3c7b3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:23:58 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 09 Jun 2021 18:25:08 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jdk_x64_windows_openj9_8u292b10_openj9-0.26.0.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jdk_x64_windows_openj9_8u292b10_openj9-0.26.0.msi ;     Write-Host ('Verifying sha256 (49e59ddbf8d9bcffbfe7c02bc4911ccc44b2426db4f4f02a3c13c3c0dadc28df) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '49e59ddbf8d9bcffbfe7c02bc4911ccc44b2426db4f4f02a3c13c3c0dadc28df') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:25:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
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
	-	`sha256:9269fb7af7bf2a450c6528fd370ef3c681ebe5a541d855609c75adf984ed4711`  
		Last Modified: Wed, 09 Jun 2021 19:32:05 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f98d3ae58bf9195cabfbe071eb0bae1a5ad20a0eb09e3230ebfa930508a188`  
		Last Modified: Wed, 09 Jun 2021 19:32:26 GMT  
		Size: 219.4 MB (219381338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8efeb70b8d3b250a24c9969112e02e1eaf58ff7d8bed3ba370e3afe32012`  
		Last Modified: Wed, 09 Jun 2021 19:32:05 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jdk-openj9-0.26.0-windowsservercore` - windows version 10.0.14393.4467; amd64

```console
$ docker pull adoptopenjdk@sha256:395c5a240bd3e9bbf8bff3c3b122f0f2fddb2da0f072af06b0efbbb7a71cb303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6485050537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12309633fcfb6029d5981e20c55d54ca2ad86a74715234c3b038880474dd595`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:25:25 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 09 Jun 2021 18:27:31 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jdk_x64_windows_openj9_8u292b10_openj9-0.26.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jdk_x64_windows_openj9_8u292b10_openj9-0.26.0.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (49e59ddbf8d9bcffbfe7c02bc4911ccc44b2426db4f4f02a3c13c3c0dadc28df) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '49e59ddbf8d9bcffbfe7c02bc4911ccc44b2426db4f4f02a3c13c3c0dadc28df') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:27:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
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
	-	`sha256:73a2d3d9f80a39d4e7065bd655fee7f28fc700500414b12a38ad61836e41d0c9`  
		Last Modified: Wed, 09 Jun 2021 19:32:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc34255747c8b5a05f65224bbfa6dfefb291f70c3505dc4c1d7eb8e5943b26e1`  
		Last Modified: Wed, 09 Jun 2021 19:36:59 GMT  
		Size: 219.3 MB (219319008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2cdf2c732a02036dc39cc4aab545aa40b4b9946a70065122c0a8df3f5389a0`  
		Last Modified: Wed, 09 Jun 2021 19:32:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
