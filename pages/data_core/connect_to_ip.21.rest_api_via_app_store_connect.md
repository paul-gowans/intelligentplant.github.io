## Configuring SQL tag search statement

When configuring your own SQL statement to perform a tag search make
sure to include 3 columns in your query: **Name** - column for tag name
search results (required). **Description** - column for tag descriptions
(optional). **UOM** - column for tag engineering units (optional).

Most importantly please add **$FILTER** variable in your LIKE filter to
make sure that results are filtered by users input. See an example
below.

An example of such query:

*SELECT ar.Name **AS Name**,ar.Definition **AS Description**,
amd.MAP\_Description **AS UOM**, amd.MAP\_SomeColumn FROM all\_records
AS ar INNER JOIN AtMapDef as amd ON ar.Definition =
amd.MAP\_DefinitionRecord WHERE ar.Name LIKE '**$FILTER**' ORDER BY
ar.Name *
