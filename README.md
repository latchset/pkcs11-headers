# PKCS#11 Headers
Free and Open Source Compatible Headers

In the 'public-domain' directory there is a set of headers that are
functionally equivalent to the standard ones but are placed in the
Public Domain for anyone to use as they see fit.

These headers have been rewritten from scratch to be equivalent to the
corresponding Oasis' ones. This is done because there are claims that
Oasis licensing is not fully Open Source, and Debian (for example)
does not accept code that includes the original headers.

The rewritten headers are a functional replacement only and intentionally
do not include any documentation string of any sort.
They are a bare functional interface with as few copyrightable features
as possible.

This repository contains a copy of Oasis's headers in the directory 'oasis'.
Oasis's original headers are the normative headers, any functional discrepancy
in the public-domain directory replacements is a bug.

# Use

Copy the header for the version of the interface you want to use in your
project and use as is or modified. Later headers are backwards compatible,
so the latest version should be preferred.

If compiling on 32-bit Windows, ensure your calling convention is set to
__cdecl for the functions you are exporting.

These headers guard deprecated declarations behind a define, for older code
bases you can define PKCS11_DEPRECATED to get access to deprecated names.

No other macro declaration is needed.

# NOTE about 3.2 headers

This work was committed in preparation for the upcoming 3.2 standard.

The OASIS PKCS#11 TC has completed its work on 3.2, but the standardization
process includes a rather slow editorial process that follows the technical
committee work. That process has started but will likely take several months
before it completes. Nonetheless drafts of the standard are available and no
more technical work is planned.

This means these headers are very unlikely to change at this point and they
can be use to prepare code for 3.2 support.
