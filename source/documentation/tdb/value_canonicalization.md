---
title: TDB Value Canonicalization
---

TDB canonicalizes certain XSD datatypes. The value of literals of
these datatypes is stored, not the original lexical form. For
example, `"01"^^xsd:integer`, `"1"^^xsd:integer` and
`"+001"^^xsd:integer` are all the same value and are stored as the
same RDF literal. In addition,
[derived types](http://www.w3.org/TR/xmlschema-2/#built-in-derived "http://www.w3.org/TR/xmlschema-2/#built-in-derived")
for integers are also understood by TDB. For example,
`"01"^^xsd:integer` and `"1"^^xsd:byte` are the same value.

When RDF terms for these values are returned, the lexical form will
be the canonical representation.

Only certain ranges of values are directly encoded as values. If a
literal is outside the canonicalization range, its lexical
representation is stored. TDB transparently switches between value
and non-value based literals in graph matching and filter
expressions; non-canonicalized and canonicalized values will be
compared as needed.

(Future versions of TDB may increase the ranges canonicalized.)

The datatypes canonicalized by TDB are:

-   XSD decimal (canonicalized range: 8 bits of scale, signed 48
    bits of value)
-   XSD integer (canonicalized range: 56 bits)
-   XSD dateTime (canonicalized range: 0 to the year 8000,
    millisecond accuracy, timezone to 15 minutes).
-   XSD date (canonicalized range: 0 to the year 8000, timezone to
    15 minutes).
-   XSD boolean (canonicalized range: true and false)
