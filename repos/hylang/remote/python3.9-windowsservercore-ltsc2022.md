## `hylang:python3.9-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:f527df457bc40fe51c138a81095ef1200f901200d33563a2478f9e1c740b44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `hylang:python3.9-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull hylang@sha256:59c97e4601e288e5b8ad43d6f3b643bbf9b314f3f75db9401fec0f761366d2fb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2265149481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49653e9632b390228a47bc30a2e81377ba0515f1331a8d95b38002cf364b02a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 00:18:26 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 20 Jan 2022 00:32:20 GMT
ENV PYTHON_VERSION=3.9.10
# Thu, 20 Jan 2022 00:32:21 GMT
ENV PYTHON_RELEASE=3.9.10
# Thu, 20 Jan 2022 00:33:54 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 20 Jan 2022 00:33:56 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 20 Jan 2022 00:33:57 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 20 Jan 2022 00:33:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Thu, 20 Jan 2022 00:34:00 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Thu, 20 Jan 2022 00:34:58 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 20 Jan 2022 00:34:59 GMT
CMD ["python"]
# Thu, 20 Jan 2022 01:01:25 GMT
ENV HY_VERSION=1.0a4
# Thu, 20 Jan 2022 01:01:26 GMT
ENV HYRULE_VERSION=0.1
# Thu, 20 Jan 2022 01:02:03 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 20 Jan 2022 01:02:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12065e818a142b555fc680a1b49a6821fbe7e8cc183fcb2210bfb689cb21ac99`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56d8cf17ed6e3db2d6ef7b8c37801c7644e2dbb511361f88cf8fa42510d666e`  
		Last Modified: Thu, 20 Jan 2022 00:42:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b22242f818cc6d947132fdbf92a7333302eb9d55c3db03cf60c5e987a127b46`  
		Last Modified: Thu, 20 Jan 2022 00:42:36 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71bb83bb5f7cc4e010ac27bfc4fd199102fa5f3c7e9002acb98816d8b60fa44`  
		Last Modified: Thu, 20 Jan 2022 00:42:43 GMT  
		Size: 50.0 MB (50007388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28878e8142d775548657189791a0ad56f6d740a5227f23eeed29c5b95cf4c978`  
		Last Modified: Thu, 20 Jan 2022 00:42:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176ed1171e766172751ab633dda8302078c313d3a02def0c783ab70722ae0161`  
		Last Modified: Thu, 20 Jan 2022 00:42:34 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2124b6ca52efa20607be7647ec60ef8ea9342dad7f7d87c54ff4f441db913f69`  
		Last Modified: Thu, 20 Jan 2022 00:42:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc6affcfd94b0edc7f252b80ecaa498745eec32475d6be7e06bacbf13b54e1d`  
		Last Modified: Thu, 20 Jan 2022 00:42:33 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789f5b975a4eb6cb7cf19c0fb47d482d62fbaac24e87f4dbf7b5aa1c8d4e45da`  
		Last Modified: Thu, 20 Jan 2022 00:42:36 GMT  
		Size: 6.5 MB (6493194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dc5ea3348e941d894a25aaf356217e157092c6bbe626e73d8fffee4246f2dd`  
		Last Modified: Thu, 20 Jan 2022 00:42:34 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529a1dd7254504d93948b96b0246f311afd322f3629a39c9368a8fb8467209a8`  
		Last Modified: Thu, 20 Jan 2022 01:04:21 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f998b2a110ce1603a57c85623edeb79e0ca1554cbfab4124b6f9173fc5f95d2`  
		Last Modified: Thu, 20 Jan 2022 01:04:21 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa20874ae745017e6305147d3cc28ee594050939add310a51214defa8859ef2c`  
		Last Modified: Thu, 20 Jan 2022 01:04:22 GMT  
		Size: 1.1 MB (1132114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8da4b48173d39d1ee64143e756690b837c4fd3e4bbf23d92d8b0c15703a755`  
		Last Modified: Thu, 20 Jan 2022 01:04:21 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
