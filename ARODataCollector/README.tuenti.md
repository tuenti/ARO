#How to build the ARODataCollector app

**Build libpcap and tcpdump**
1. Install the android ndk: http://developer.android.com/tools/sdk/ndk/index.html
1. Run `nkd-build` from this directory.

This will build the library and binary for both arm and x86 architectures.


**Build the app**

At present the app must be built to support just one of the architectures: arm or x86. If you want it to be run in a VM, you'll most likely want the x86 version.

1. Build libpcap and tcpdump if you haven't done so yet.
1. Copy the binary for the architecture of your choice to `res/raw`. E.g: `cp libs/x86/tcpdump res/raw/tcpdump`
1. Run `ant debug`
