# TCLAP - Templatized Command Line Argument Parser

This is a simple C++ library that facilitates parsing command line
arguments in a type independent manner.  It doesn't conform exactly
to either the GNU or POSIX standards, although it is close.  See
docs/manual.html for descriptions of how things work or look at the
simple examples in the examples dir.

To find out what the latest changes are read the NEWS file in this directory.


Any and all feedback is welcome to:  Mike Smoot <mes@aescon.com>

-------------------------------------------------------------------------------

This repository is a "mirror" of the original host, with a _minimal_ CMake build
system.  See the official website here: http://tclap.sourceforge.net/

At this time the current version is 1.2.2.  _Please raise an issue if a newer
version bas been released on sourceforge but not here_.

When adding the submodule, each version will be tagged to correspond with
sourceforge releases.  Check `git tag -l` and `checkout` the corresponding
release tag, e.g. `git checkout v1.2.2`.

# Submodule Usage

This repository is used as a submodule, and includes a _minimal_ CMake build
system that defines an interface target.  **The CMake build system does not
perform installations**, see
[Installation and Running Tests](#installation-and-running-tests).

## For CMake 3.0+

```cmake
add_subdirectory(path/to/tclap)

# Option 1: you have a target to link with
target_link_libraries(your_target tclap)

# Option 2: if you need to add to a list or something
get_target_property(TCLAP_INCLUDE_DIRS tclap INTERFACE_INCLUDE_DIRECTORIES)
# You can now use ${TCLAP_INCLUDE_DIRS}
```

## For CMake 2.x

TCLAP is a header-only library, so just include the right path (but do **not**
`add_subdirectory`).

```cmake
include_directories("${CMAKE_CURRENT_SOURCE_DIR}/path/to/tclap/include")
```

# Installation and Running Tests

Please use the original `configure` scripts.  See the `INSTALL` file for more
information.  For running tests, `./configure && make check`.
