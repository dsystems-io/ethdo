# Troubleshooting

## Compilation problems

### gcc not found
### cannot find -lstdc++

This is usually an error on linux systems.  If you receive errors of this type your computer is missing some files to allow `ethdo` to build.  To resolve this run the following command:

```sh
sudo apt install build-essential libstdc++6
```

and then try to install `ethdo` again.

## ethdo not found after installing

This is usually due to an incorrectly set path.  Go installs its binaries (such as `ethdo`) in a particular location.  The defaults are:

  - Linux, Mac: `$HOME/go/bin`
  - Windows: `%USERPROFILE%\go\bin`

You must add these paths to be able to access `ethdo`.  To add the path on linux or OSX type:

```sh
export PATH=$PATH:$(go env GOPATH)/bin
```

and on Windows type:

```sh
setx /M path "%PATH%;%USERPROFILE%\go\bin"
```
