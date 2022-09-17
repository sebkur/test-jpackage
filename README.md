# Hello jpackage

Run:

    ./gradlew run

Package:

    ./gradlew jpackage

In case the jpackage task fails, make sure to run this with `--info` to see
output of the jpackage executable.

On Windows, make sure to download https://github.com/wixtoolset/wix3/releases/download/wix3112rtm/wix311-binaries.zip
and to unpack that for example to ~/Downloads/wix311binaries. You need
to have that directory on your PATH in order to successfully build an installer.
On MinGW/Git Bash you can type this:

    PATH=$PATH:~/Downloads/wix311-binaries ./gradlew jpackage --info

On PowerShell, this works:

    $env:path += ";$env:userprofile\Downloads\wix311-binaries"
    .\gradlew jpackage --info
