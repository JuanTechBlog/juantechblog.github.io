---
title: "How to install Hugo on Windows 11."
description: "I just learned how to install Hugo with Go/Golang and Git."
date: "2024-03-16"
tags: ["Hugo", "Windows 11", "Go", "Golang", "Git"]
draft: false
ShowToc: true
draft: false
canonicalURL: "https://juanstechblog.blogspot.com/2024/03/how-to-install-hugo-on-windows-11.html"
cover:
    image: how-to-install-hugo-on-windows11.webp
    alt: "How to Install Hugo on Windows 11 cover"
    caption: "How to Install Hugo on Windows 11"
    relative: true
---

I recently switched from macOS(Hackintosh) to Windows 11. So, a lot of things need to be installed again. Hugo is one of the tools that I use to preview my blog posts or edit some theme settings.

To install the Hugo extended edition, we will only install Go/Golang and Git.

Let's install it.

## Install Go/Golang

Download the Go/Golang installer from the Go [website](https://go.dev/dl/).

Run it and proceed until complete.

To check the installation by executing the command below:
```shell
> go version
```

The result should be something like this:
```shell
go version go1.22.1 windows/amd64
```

## Install Git

Download the Git installer from the [official website](https://git-scm.com/download/win).

Run it and proceed until complete. Most of the settings are default, I only change the text editor to Visual Studio Code.

Afterward, we open the terminal to verify the installation as below:
```shell
> git --version
```

The result should be something like this:
```shell
git version 2.44.0.windows.1
```

## Install Hugo
Download the Hugo extended edition binary from Hugo's GitHub [repository](https://github.com/gohugoio/hugo/releases).


![Copy Hugo's binary folder path.](copy-hugo-binary-folder-address.webp)

Extract the binary's compressed file. I take a further step to place it in the Program Files, Disk C, and copy the folder path.

![Search "Edit the system environment variables" in Windows Search.](windows-search-edit-environment-variables.webp)

Press the Win key, search "Edit the system environment variables", and press Open.

![Click the Environment Variables button, select Path, and click the edit button in the User Variables section.](click-environment-variables-select-path-in-user-variables-and-click-edit-button.webp)

Click the Environment Variables button, select Path, and click the edit button in the User Variables section.

![Paste the Hugo binary's folder path as new environment variable.](add-hugo-extended-binary-folder-in-environment-variable.webp)

Click the New button and paste the Hugo extended edition binary's folder path.

Click the OK button twice to save the changes.

Open the terminal and execute this command to verify the installation.

```shell
> hugo version
```

The result should be something like this:
```shell
hugo v0.123.8-5fed9c591b694f314e5939548e11cc3dcb79a79c windows/amd64 BuildDate=2024-03-07T13:14:42Z VendorInfo=gohugoio
```


