## `hylang:python3.10-rc-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:27a22777b86300de4ba675ea7fd034281bf3344578727a71bd294b04a37493d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `hylang:python3.10-rc-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull hylang@sha256:cb8e744a15d3b99b224d3c7a3dc3790fec0892cd8abf0ee78fb3564fb89fb3d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6324494456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ff3a6bd8d93a21c70712be6979faa6f39d1bbd843d39a96590420136fdee6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 16:04:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Jun 2021 16:04:36 GMT
ENV PYTHON_VERSION=3.10.0b2
# Wed, 09 Jun 2021 16:04:39 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 09 Jun 2021 16:07:09 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:07:11 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Wed, 09 Jun 2021 16:07:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Wed, 09 Jun 2021 16:07:16 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Wed, 09 Jun 2021 16:09:10 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:09:12 GMT
CMD ["python"]
# Wed, 09 Jun 2021 16:37:48 GMT
ENV HY_VERSION=1.0a1
# Wed, 09 Jun 2021 16:39:38 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 09 Jun 2021 16:39:40 GMT
CMD ["hy"]
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
	-	`sha256:43dfa55ab4db6f7cde43273b96f1f6819cd2c3cea34c5ad67065d7ab4210320a`  
		Last Modified: Wed, 09 Jun 2021 16:26:18 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c16f6000b5eacc17ec60e0b2f39bd8604d967f0632ee5d4c2b714b113f9614e`  
		Last Modified: Wed, 09 Jun 2021 16:26:20 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072a93a122fd445a0e577720c18fb4c3167dfd4b61e354f8a2c4a00ce9260f1f`  
		Last Modified: Wed, 09 Jun 2021 16:26:18 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a196ebb450e5b27a63c9052453062b7dbfe47554febe38d396f940e67e3a609`  
		Last Modified: Wed, 09 Jun 2021 16:26:28 GMT  
		Size: 51.2 MB (51157875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103e8d8feec3e6756d6e3f7202417058d130363ccb227805bc7b8980023a732`  
		Last Modified: Wed, 09 Jun 2021 16:26:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33017fd9d39c9470133b266bba4427632dc22927c2116aca7a3746208e068bf4`  
		Last Modified: Wed, 09 Jun 2021 16:26:16 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc128097d102fc960886f2cca2dfc8d707ea057b8dff647958f76989383f30`  
		Last Modified: Wed, 09 Jun 2021 16:26:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21b932e593d618256d81d0e0ed724ee08258ba73940f40d9bd6e5672cb3cc92`  
		Last Modified: Wed, 09 Jun 2021 16:26:18 GMT  
		Size: 6.4 MB (6431439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c429a9d681a82a694d49f658926f213f0bea9fd243b1499690f212dc1c2ba4b0`  
		Last Modified: Wed, 09 Jun 2021 16:26:16 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fab19220fa3d33bf1d270a9812cba30c1b28281f80714c213a5380aac38faa`  
		Last Modified: Wed, 09 Jun 2021 16:43:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cebbcbfad97a43b96ca0b64ec2aee25943cc72373b81a8395e7eadb1eae143`  
		Last Modified: Wed, 09 Jun 2021 16:43:21 GMT  
		Size: 1.2 MB (1163731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f52d1337010b0093f600a0ea6e80aa62daf6902a8820a8cb8513069f779be56`  
		Last Modified: Wed, 09 Jun 2021 16:43:21 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
