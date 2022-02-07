<!------------------------------------------------------------------------------
--
-- Copyright (C) 2022 Kevin Matthes
--
-- This program is free software; you can redistribute it and/or modify
-- it under the terms of the GNU General Public License as published by
-- the Free Software Foundation; either version 2 of the License, or
-- (at your option) any later version.
--
-- This program is distributed in the hope that it will be useful,
-- but WITHOUT ANY WARRANTY; without even the implied warranty of
-- MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-- GNU General Public License for more details.
--
-- You should have received a copy of the GNU General Public License along
-- with this program; if not, write to the Free Software Foundation, Inc.,
-- 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
--
----
--
--  FILE
--      README.md
--
--  BRIEF
--      Important information regarding this project.
--
--  AUTHOR
--      Kevin Matthes
--
--  COPYRIGHT
--      (C) 2022 Kevin Matthes.
--      This file is licensed GPL 2 as of June 1991.
--
--  DATE
--      2022
--
--  NOTE
--      See `LICENSE' for full license.
--
------------------------------------------------------------------------------->

# docs-snippets

## Summary

A collection of common documentation configuration files.

## License

This project's license is **GPL 2** (as of June 1991).  The whole license text
can be found in `LICENSE` in the main directory of this repository.  The brief
version is as follows:

> Copyright (C) 2022 Kevin Matthes
>
> This program is free software; you can redistribute it and/or modify
> it under the terms of the GNU General Public License as published by
> the Free Software Foundation; either version 2 of the License, or
> (at your option) any later version.
>
> This program is distributed in the hope that it will be useful,
> but WITHOUT ANY WARRANTY; without even the implied warranty of
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
> GNU General Public License for more details.
>
> You should have received a copy of the GNU General Public License along
> with this program; if not, write to the Free Software Foundation, Inc.,
> 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

When compiling a printable version of this documentation using Pandoc, the full
license will be attached automatically to the resulting document.  This can be
invoked by calling `repository-manual.m`.

## Description

Any good project should have at least a reasonable minimum of description.
Therefore, plenty of automatic documentation creation were developed in order
to make the process of writing a manual easier.  Many of those are specific to
one certain language, such as Haddock for Haskell or JavaDoc for Java.  Some
even support multiple languages like Doxygen does for C-like languages.

All of the systems have in common that they generate the intended documentation
from the source code of the project, evaluating some certain comments placed in
there.  Furthermore, they might be instructed to mind certain settings when
writing the documentation; one of the most common settings therefore is the
actual output directory.  Systems like Haddock and JavaDoc accept such settings
as command line arguments when called, Doxygen, in contrast, reads the
preferences from a configuration file.

Not only these configurations, no matter if processed whether by command line
arguments or by configuration files, but also the documenting comments, often
named "docstrings", will produce redundancy since most of the content will be
equal for numerous projects.

The purpose of this repository is it therefore to provide some frequently used
configuration settings and docstring patterns for several languages and
documentation systems.  They can be considered sample templates but also be
adjusted to the needs of a certain project and / or repository which binds this
one as a submodule.

## Software Requirements

This repository does not contain any source code, so there are no major software
requirements.  However, it is possible to compile a printable description of the
repository's READMEs as well as the LICENSE.  Therefore, one needs the following
applications:

| Requirement       | Type          | Role                              |
|:------------------|:-------------:|:----------------------------------|
| GNU Octave        | application   | execution of the provided scripts |
| Pandoc            | application   | compilation of repository manual  |
| `texlive-full`    | package       | compilation of repository manual  |

The compilation of such an **optional** repository manual can be invoked by just
calling:

```
octave repository-manual.m
# or
octave-cli repository-manual.m
```

<!----------------------------------------------------------------------------->
