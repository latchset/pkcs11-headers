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
project and use as is or modified. Later headers are bacwards compatible,
so the latest version should be preferred.

The header does not include any optional architecture specific directive.

On windows the header should wrapped in #pragma statements for packing
(ex: #pragma pack(1))

The header does not wrap in extern "C" {}, so C++ projects will have to do
that on their own.

Thse headers guard deprecated declarions behind a define, for older code
bases you can define PKCS11_DEPRECATED to get access to deprecated names.

No other macro declaration is needed.
