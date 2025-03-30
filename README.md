# Catalog for JahnTech Package Manager for webMethods Integration

The JahnTech Package Manager for webMethods Integration allows the
automation of work with packages for Integration Server and
Microservices Runtime.

Functionality includes:

- Checkout package source code from Git into workspace, symlink 
  against `./packages` directory of IS/MSR, and compile+frag
  the Java code
- Install ZIP archive of package in IS/MSR (planned).
- Group packages into applications for bulk operations
- Operate your own catalog

Package information is maintained with a catalog, that contains
a file (name: `pkg_*`) for each package. This GitHub project serves as a
demonstration and also makes it easy for people to work
with the opensource packages from JahnTech.

In addition to working with individual packages, it is also possible
to group them together into applications. This is a convenient
way to organize projects. By getting the the project source from
VCS one can set up a new development environment with a single command.

