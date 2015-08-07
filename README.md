[![Build Status](https://travis-ci.org/maddenp/nlh.svg)](https://travis-ci.org/maddenp/nlh)

nlh
===

A Ruby library and command-line tool for handling (querying & modifying) Fortran namelist files.

###Please use the [nml](https://github.com/maddenp/nml) tool instead, if possible.

### Usage

`nlh.rb file namelist key [value]`

### Notes

The `file` containing the namelist(s) must exist, though it may be empty. For command-line usage, omitting the optional 'value' argument performs a lookup; supplying it performs a modification. Missing namelists or keys are created as needed. For programmatic usage, see the unit-test script, `unit`, for examples.

I fully expect that some valid Fortran namelists will not be parsed correctly by this code. I'm planning to write a replacement using a [PEG](http://bford.info/packrat) toolkit, which will hopefully be robust. But this tool covers much practical ground, and emits (I believe) namelists that are standard-conformant.

Please note that, when processing an existing namelist file, comments are removed and namelists are reformatted (in a hopefully useful way).
