# Catalog for JahnTech Package Manager for webMethods Integration (JTWPM)

The [JahnTech Package Manager for webMethods Integration (aka JTWPM)](https://jahntech.com/jtwpm) is a free-of-charge tool for the command line, which allows the
automation of work with packages for
Integration Server and Microservices Runtime.
Below is a quick overview and for further information you should
have a look at the [product page](https://jahntech.com/jtwpm).

## Supported operating systems

JTWPM works on macOS, Linux, and Windows and is implemented as a Bash
script. Bash comes out-of-the-box on Linux and macOS. On Windows
development environments it is usually installed as part of [Git for Windows](https://git-scm.com/install/windows)
(Git Bash).

So in most cases no additional installation is needed.
(Not having to install something like Node, Python, Ruby, etc. has
been the primary reason to use Bash.)
On Windows you can also Cygwin or MSYS2 to get a Bash shell.
WSL does not work however, due to the way paths are translated
between environments.

## Functionality

### Packages

Functionality includes:

- Checkout package source code from Git into workspace, symlink
  against `./packages` directory of IS/MSR, and compile+frag
  the Java code
- Install ZIP archive of package in IS/MSR
- Group packages into applications for bulk operations
- Operate your own catalog
- Get homepage and support URLs for package
- Update package sources from Git, compile+frag Java, and reload package
- Manage external jar files (incl. use of Maven POM files)
- Switch between different workspaces/projects
- Start/stop Integration Server and watch `server.log`

Package information is maintained with a catalog, that contains
a file (name: `pkg_*`) for each package. This GitHub project serves as a
demonstration and also makes it easy for people to work
with the opensource packages from JahnTech.

To get the homepage of the packge just run `jtwpm pkg home <PACKAGE>`.

Example:

```bash
jtwpm pkg homepage WxGenerate
```

### Applications/projects

In addition to working with individual packages, it is also possible
to group them together into applications (name: `app_*`). This is a convenient
way to organize projects you can set up a new development environment with a single command.

Try

```bash
jtwpm app src Demos
```

and and you will get the following packages in one go:

- DemoBootstrapUI
- JT_Demo_DebugDSP
- Log4jDemo

---
This catalog repo is available under an Apache 2.0 license.

JTWPM itself, while being provided free of charge, is not open source and comes
with a commercial license. For details, please have a look at the
[product page](https://jahntech.com/jtwpm).


---
webMethods® is a registered trademark of International Business Machines Corporation (“IBM”).
