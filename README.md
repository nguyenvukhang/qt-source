# Qt source, initialized

The main value of this repository lies over at its [releases].

This tarball is produced by:

1. Cloning the qt source code at a particular version.
2. Running `init-repository` with only `qtbase` selected.

The produced tarball is always standardized to this format:

```sh
qt-<github runner os>-<qt version>.tar.gz
# qt-ubuntu-22.04-6.2.0.tar.gz
```

For a list of all GitHub runner's operating systems, go
[here][gh-images].  
For a list of all valid Qt version numbers, go
[here][qt-refs].

For a list of operating system-version number pairs supported, head
over to the this repository's [releases], and check if it's
built.

If it isn't, either open a Pull Request, or just fork this repository
and make changes to `./.github/workflows/main.yml`.

### Scripting

To download it, here are two useful links:

```sh
# using a particular release
https://github.com/nguyenvukhang/qt-source/releases/download/v0.0.1/qt-ubuntu-22.04-6.2.0.tar.gz
# using the latest release
https://github.com/nguyenvukhang/qt-source/releases/latest/download/qt-ubuntu-22.04-6.2.0.tar.gz
```

### Recommended use

```sh
curl -fLo q.tar.gz https://github.com/nguyenvukhang/qt-source/releases/download/v0.0.1/qt-ubuntu-22.04-6.2.0.tar.gz

mkdir qt_src
mv q.tar.gz qt_src

# unpack and delete the tarball
cd qt_src
tar -xzf q.tar.gz
rm q.tar.gz
```

[releases]: https://github.com/nguyenvukhang/qt-source/releases
[gh-images]: https://github.com/actions/runner-images#available-images
[qt-refs]: https://code.qt.io/cgit/qt/qt5.git/refs
