Version 1.2.0:  August 17, 2018
--------------------------------------------------------------------------------

+ Updated schema set to v1.2.
+ Several improvements to the ``validate_rearrangement`` function.
+ Changed behavior of all `airr.interface` functions to accept a file path
  (string) to a single Rearrangement TSV, instead of requiring a file handle as
  input.
+ Added ``base`` argument to ``RearrangementReader`` and ``RearrangementWriter``
  to support optional conversion of 1-based closed intervals in the TSV to python-style
  0-based half-open intervals. Defaults to conversion.
+ Added the custom exception ``ValidationError`` for handling validation checks.
+ Added the ``validate`` argument to ``RearrangementReader`` which will raise
  a ``ValidationError`` exception when reading files with missing required
  fields or invalid values for known field types.
+ Added ``validate`` argument to all type conversion methods in ``Schema``,
  which will now raise a ``ValidationError`` exception for value that cannot be
  converted when set to ``True``. When set ``False`` (default), the previous
  behavior of assigning ``None`` as the converted value is retained.
+ Added ``validate_header`` and ``validate_row`` methods to ``Schema`` and
  removed validations methods from ``RearrangementReader``.
+ Removed automatic closure of file handle upon reaching the iterator end in
  ``RearrangementReader``.

Version 1.1.0:  May 1, 2018
--------------------------------------------------------------------------------

Initial release.