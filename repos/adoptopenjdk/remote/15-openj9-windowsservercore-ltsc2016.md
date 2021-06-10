## `adoptopenjdk:15-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:22df8e05ec8dab8f7005540ce0fbd2132cafd7429af0f8d97729a9ad878117c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `adoptopenjdk:15-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull adoptopenjdk@sha256:995e7ff7905bafd6917fb59495df0bbe8b70e8b0916f69cc445c73b29cbfa99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6644058749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb5a381b6e0d165cd80c79f64a4319e6fecb37340ab7b850301077a9535d39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:40:15 GMT
ENV JAVA_VERSION=jdk-15.0.2+7_openj9-0.24.0
# Wed, 09 Jun 2021 18:42:38 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jdk_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jdk_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (f366ebd9f9b4243a86bbf72975f9357a7fa6aec5dac40af4edd4c97ddb4d28b8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f366ebd9f9b4243a86bbf72975f9357a7fa6aec5dac40af4edd4c97ddb4d28b8') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:42:41 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 09 Jun 2021 18:42:43 GMT
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
	-	`sha256:645305aa477d3b592303dcc0ca69ab6db2671e43b1b0677131fe60cdbcbaf9de`  
		Last Modified: Wed, 09 Jun 2021 19:41:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d666edad52b53417a8f0080839fae7fcd1544acc35973204bd1a0b96076bfae2`  
		Last Modified: Wed, 09 Jun 2021 19:48:38 GMT  
		Size: 378.3 MB (378326064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4599d0ae4246e10ac8aa6430cf2d2303c9e358f50ba3a806571f34d9be451db`  
		Last Modified: Wed, 09 Jun 2021 19:41:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4debb5f2c381f8b65401fbc7150541df80450af05676c829b097cdd4e364be`  
		Last Modified: Wed, 09 Jun 2021 19:41:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
