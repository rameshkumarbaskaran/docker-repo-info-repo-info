## `adoptopenjdk:8-jre-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:b38176ab49d2d9b3ad41eb091df05cf0b84e636c059a73f75bd1b915bb510988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `adoptopenjdk:8-jre-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull adoptopenjdk@sha256:9a7cf325e87caa0db9ed8e877db01cbec4b147213d9fedf1af66e54560073926
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6356923330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456dd1037a52e523785ac9d5f46e94f9f65baae925b5e125014e9bf534322772`
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
# Wed, 09 Jun 2021 18:30:38 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_windows_openj9_8u292b10_openj9-0.26.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_windows_openj9_8u292b10_openj9-0.26.0.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (8decae9e065946cfc9a4b7f3c0ed61cfc6fe3076cdcbbbece33ef39c9ccef6e3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8decae9e065946cfc9a4b7f3c0ed61cfc6fe3076cdcbbbece33ef39c9ccef6e3') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:30:41 GMT
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
	-	`sha256:9e3410d0d98344ab7a29991f5cd3cb1600d9f04e43d0abe32a5711307ebfb49b`  
		Last Modified: Wed, 09 Jun 2021 19:37:49 GMT  
		Size: 91.2 MB (91191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df09a41fd2998c41da3af244805476451668694a1f0c520d46d5241ee795e45`  
		Last Modified: Wed, 09 Jun 2021 19:37:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
