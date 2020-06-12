**GET
Gestalt/api/data/values/{dsn}?tag={tag\_name\_1}\&tag={tag\_name\_2}\&function={function}\&start={start}\&end={end}\&step={step}
**

Performs a tag data query on a data source.

*For .NET developers, we recommend that you use the
`IntelligentPlant.AppStore.Client` NuGet package to query for data,
available on the App Store NuGet feed
(<https://appstore.intelligentplant.com/nuget/nuget/>).*

For the *function* field supported values vary from driver to driver,
but it's safe to assume that the following values will be supported:

  - **RAW** - for raw historical data (**not recommended** due to the
    potential high volume of data returned)
  - **NOW** - for the current snapshot value
  - **INTERP** - for interpolated data
  - **PLOT** - a display-friendly aggregation for when you want to
    display a trend on the screen
  - **MIN** - minimum value calculated at each sample interval over a
    time range
  - **MAX** - maximum value calculated at each sample interval over a
    time range
  - **AVG** - mean value calculated at each sample interval over a time
    range.

For `start` and `end`, you can specify either an absolute value or a
relative value. Absolute values should be specified in ISO 8601 format
(i.e. `yyyy-MM-ddTHH:mm:ss`). You can also include a suffix of `Z` to
indicate a UTC time stamp, or you can specify an offset from UTC. If no
time zone information is provided, the date is assumed to be UTC. For
example, if you wanted to specify 3:30:35am on 01 August 2017 in Central
US time, you could specify `2017-08-01T03:30:35-06:00`.

Relative values can be specified using `*` to represent the current
time. For example: `*-1d` = "1 day before current time", `*-27.5m` =
"27.5 minutes before current time", and so on. Possible time units when
specifying a relative time stamp are: `d`, `h`, `m`, `s`, `ms`.

For the current value, specify `NOW` for the `function` parameter. When
you use `NOW`, you don't need to specify a start or end time. For
example, to get the current snapshot value for tags called *Tag1* and
*Tag2*, you would use:

`gestalt/api/data/values/{my_dsn}?function=NOW&tag=Tag1&tag=Tag2`

To get all raw data in a time period, you use the `RAW` function. When
asking for raw data, you don't need to specify a sample interval or a
point count:

`gestalt/api/data/values/{my_dsn}?function=RAW&tag=Tag1&start=*-1d&end=*`

`RAW` queries are **strongly discouraged**, due to the potentially large
data set that must be sent over the wire.

For other functions, you need to provide either a `step` parameter that
specifies the sample interval (e.g. `1m`, `5m`, `8h`, `3d`), or a
`points` parameter that specified the number of samples you want to be
returned:

`gestalt/api/data/values/{my_dsn}?function=INTERP&tag=Tag1&tag=tag2&start=*-1d&end=*&step=1h`
`gestalt/api/data/values/{my_dsn}?function=PLOT&tag=Tag1&tag=tag2&start=*-1d&end=*&points=750`

More info on App Store API can be found
<https://appstore.intelligentplant.com/ApiHelp>
