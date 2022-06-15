## `eclipse-temurin:18-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f10a9f7dc14177c2f50d4a22fe8906de169c71e8185391df7578d82453cf75ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:18-windowsservercore` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:f193a6e6d85035a8948828cb6a98802bc1661f7b23ccba93536aa1bd40cdc31b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2633884387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c152371d7a6b0adce28830d7b732c18b8b6b779cfbe64aefb93bb7a89f55bc5c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 17:56:49 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 15 Jun 2022 17:57:48 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_windows_hotspot_18.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_windows_hotspot_18.0.1_10.msi ;     Write-Host ('Verifying sha256 (6915a747550facec2cbfb22f6ae8f3c47dfcde857e69cf94409b664f81415e69) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6915a747550facec2cbfb22f6ae8f3c47dfcde857e69cf94409b664f81415e69') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 Jun 2022 17:58:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 15 Jun 2022 17:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3313ad9d8ab04ccbddc0a27c01c2ab5f5ca7d4d76211c06eb0cacaea5a23fb6`  
		Last Modified: Wed, 15 Jun 2022 18:53:17 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a2185b89157de2c84ae5350fc61f190d5136d925a3308d9c619318aa9d1358`  
		Last Modified: Wed, 15 Jun 2022 18:59:34 GMT  
		Size: 354.8 MB (354839557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e592fb8818e2735688e8ede524e21aa7dc4bb5fa37d899ebe52c8ea94563875f`  
		Last Modified: Wed, 15 Jun 2022 18:53:17 GMT  
		Size: 576.7 KB (576684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb2b7eba489bad0464ddc55e1ec0a471c7393b2d789e556426ad1719c2f70a`  
		Last Modified: Wed, 15 Jun 2022 18:53:16 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-windowsservercore` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:1298f629160ad4333113d69f9f348ecedbd55b7200b9bf0db98db55060a9d164
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3021661195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d158ed9b0cb1f6766d4d7d9ecdcd4c00b4451c18b5811e84758c7149257d62`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 17:58:19 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 15 Jun 2022 18:01:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_windows_hotspot_18.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_windows_hotspot_18.0.1_10.msi ;     Write-Host ('Verifying sha256 (6915a747550facec2cbfb22f6ae8f3c47dfcde857e69cf94409b664f81415e69) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6915a747550facec2cbfb22f6ae8f3c47dfcde857e69cf94409b664f81415e69') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 Jun 2022 18:03:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 15 Jun 2022 18:03:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf3d2e317c9dbd7cb4498e4d27d201324aaa492f7100ad780994fc9e1343876`  
		Last Modified: Wed, 15 Jun 2022 18:59:48 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23dd7816fb9ea7ee2892532a8f6983bc68721fb4cfe9a3ac97743a3ef297470`  
		Last Modified: Wed, 15 Jun 2022 19:06:01 GMT  
		Size: 354.6 MB (354590326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec72647ff7cad07b50f5e6800b5ba770460866858d9641456137908c365dafb`  
		Last Modified: Wed, 15 Jun 2022 18:59:52 GMT  
		Size: 3.8 MB (3786847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8724b9406d1174a06de9dd96278c600a5b80f937537557e5db13882d5c531633`  
		Last Modified: Wed, 15 Jun 2022 18:59:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
