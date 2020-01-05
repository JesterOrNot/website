# Python

> 🚧 Please help improve this guide by [editing it](https://gitpod.io/#https://github.com/gitpod-io/website/blob/master/src/docs/python_in_gitpod.md).

Gitpod comes with great support for Python builtin. Still, depending on your particular project, you might want to further optimize the experience.

## GUI Applications with wxPython
Have a super cool GUI application you are building with wxPython? Want to run it in Gitpod? Please take a look at [JesterOrNot/Gitpod-PythonGUI-Example](https://github.com/JesterOrNot/Gitpod-PythonGUI-Example)

Here is an exmaple .gitpod.Dockerfile
```dockerfile
FROM gitpod/workspace-full-vnc:latest

USER root

ARG DEBIAN_FRONTEND=noninteractive

# Install WXPython Dependencies
RUN apt-get -q update \
    && apt-get install -yq \
        freeglut3-dev \
        python3.7-dev \
        libpython3.7-dev \
        libgl1-mesa-dev \
        libglu1-mesa-dev \
        libgstreamer-plugins-base1.0-dev \
        libgtk-3-dev \
        libnotify-dev \
        libsdl2-dev \
        libwebkit2gtk-4.0-dev \
        libxtst-dev \
        libgtk2.0-dev \
    && sudo rm -rf /var/lib/apt/lists/*

# Add wxpython itself

USER gitpod

RUN pip3 install -U -f https://extras.wxpython.org/wxPython4/extras/linux/gtk3/ubuntu-18.04/ wxPython
```
Here is an example .gitpod.yml
```yaml
image:
  file: .gitpod.Dockerfile

ports:
  - port: 6080
    onOpen: open-preview
  - port: 5900
    onOpen: ignore
  - port: 35900
    onOpen: ignore

tasks:
  - command: python3 app.py
```
