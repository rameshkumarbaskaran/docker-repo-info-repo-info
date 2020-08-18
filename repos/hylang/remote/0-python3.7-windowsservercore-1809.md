## `hylang:0-python3.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:f0cc746b3c9fd2662e20583c6f6e2a33de304d57c52110eb5c3a5cd7042fb02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `hylang:0-python3.7-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull hylang@sha256:0b737172ad5c7da71a1332669bf7e38665e81738479ff6a5ebb5aa9697727701
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407429737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6465cc5ca66859a7c3774e0579000e6302ab924c6c3ecaeb2ef62c79be5276e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Aug 2020 04:19:14 GMT
ENV PYTHON_VERSION=3.7.9
# Tue, 18 Aug 2020 04:19:15 GMT
ENV PYTHON_RELEASE=3.7.9
# Tue, 18 Aug 2020 04:20:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 18 Aug 2020 04:21:00 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 18 Aug 2020 04:21:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 18 Aug 2020 04:21:02 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 18 Aug 2020 04:21:52 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 18 Aug 2020 04:21:53 GMT
CMD ["python"]
# Tue, 18 Aug 2020 04:40:20 GMT
ENV HY_VERSION=0.19.0
# Tue, 18 Aug 2020 04:40:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 18 Aug 2020 04:40:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94c4b3988b4b005a8d34d1a71609d82c90c883549db148cedb7cf96610ce251`  
		Last Modified: Tue, 18 Aug 2020 04:23:20 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3e5134bf6cf21d040531fc017b28bc2fe45e5b60b8e32dd63474051762e806`  
		Last Modified: Tue, 18 Aug 2020 04:23:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd647650665a950ca8e8b1c9d6e6df02d6a2c6f0c6b07308a67cd215c245b9`  
		Last Modified: Tue, 18 Aug 2020 04:23:28 GMT  
		Size: 55.8 MB (55775066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03222a82024b13f644a31a6641734bea869b89e4a2eec58304e69ba5d454d67a`  
		Last Modified: Tue, 18 Aug 2020 04:23:16 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e5ca78493cc9680d1e06a50a46dce6d9bb0ab975e3b89e9ae215291409508`  
		Last Modified: Tue, 18 Aug 2020 04:23:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c9a4c5bffcd0d60a774a641c51442e8210f9af01c18cdd08ee4a9a2fb9c651`  
		Last Modified: Tue, 18 Aug 2020 04:23:17 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93212e8a2db25d19d27da3f07336f19568f5ddb5e920d979b2b29625c919a4b`  
		Last Modified: Tue, 18 Aug 2020 04:23:20 GMT  
		Size: 10.3 MB (10257777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19394f285ffca84487f3a45348e525e058ec28a2fa4c66d5dd1cf4d736413041`  
		Last Modified: Tue, 18 Aug 2020 04:23:17 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f525f22f32bffcd639107b8bf0e30b83cac2a6b5cdf1d1440ca3049aecdff481`  
		Last Modified: Tue, 18 Aug 2020 04:43:25 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5611707371b8fdfba1dde3b9b49b2a2a9ae7737c4fda272def67e21b86cba4`  
		Last Modified: Tue, 18 Aug 2020 04:43:27 GMT  
		Size: 5.5 MB (5519740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b830496783f98f22d2d9242ced221525fc3beadf2a6335866153405cb540e3b7`  
		Last Modified: Tue, 18 Aug 2020 04:43:25 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
