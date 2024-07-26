## Company System

Company System is a demo application that works with three build tools:

* GNU Make
* [ibmi-bob](https://ibm.github.io/ibmi-bob/#/)
* ARCAD Builder from IBM i Modernization Engine for Lifecycle Integration (Merlin)

### Setup
1. Install IBMi Repos =>   `yum install ibmi-repos`
2. Update yum packages => `yum update`
3. Install BOB => `yum install bob`
4. Create a library to save the build => `system "CRTLIB LIB(CMPSYS) TEXT('Better Object Builder test project')"`
5. Clone the repository `git clone https://github.com/ravisankar-PIO/cmpsys`
6. Go to the cloned repo directory `cd cmpsys`
7. Set the env variable to point the library that we just created `export CURLIB=CMPSYS`
8. Run the build using `makei build`

TODO.

### Build Commands

* GNU Make
* ibmi-bob
   * Project build `makei build`
   * Compile of files `makei compile -f {files}`
* ARCAD Builder
   * Project build `/QOpenSys/pkgs/bin/elias compile {branch}`
   * Compile of files `/QOpenSys/pkgs/bin/elias compile {branch} -f {files}`
