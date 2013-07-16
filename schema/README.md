# Open511 XML Schemas

We currently maintain a [RELAX NG](http://relaxng.org/) schema for the [Open511](http://www.open511.org/) XML format.

You can find this schema in `open511.rng`. `open511.rnc` is written in the RELAX NG compact syntax, and expresses the same logic as the `rng` file.

`open511.schematron` is a [Schematron](http://www.schematron.com/) document expressing some additional validation logic. RELAX NG alone is not capable of expressing all the requirements of the Open511 format, and so to determine whether a document is valid, you need to verify it against both `open511.rng` and `open511.schematron`.
