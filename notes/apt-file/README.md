# Using apt-file

If you have ever had a missing library for development purposes. One tool that
comes in most Debian based distros is `apt-file`. To install, run:

```sh
sudo apt install apt-file
sudo apt-file update
```
Very simple to use, simply:

```sh
apt-file find NAME OF MISSING LIBRARY
```
For example, let's say that you are missing the `openssl/err.h` header file
(very common btw). All one had to do is:

```sh
apt-file find openssl/err.h
```
You will receive all of the possible libraries in you apt sources that has that
file. Install the one library you actually need.
