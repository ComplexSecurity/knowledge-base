icon:material/apple

# System_profiler

Command-line utility on macOS that generates detailed reports about hardware and software configuration of the system.

## Usage

```bash
system_profiler [-listDataTypes]
system_profiler [-xml | -json] [-timeout n] [-detailLevel n]
system_profiler [-xml | -json] [-timeout n] [dataType1 ... dataTypeN]
```

## Flags

```bash
  -detailLevel n    specifies the level of detail for the report
                      mini = short report (contains no identifying or personal information)
                      basic = basic hardware and network information
                      full = all available information

  -listDataTypes    lists all the available datatypes

  -xml              generates xml output instead of plain text
                    if redirected to a file with the extension ".spx"
                    the file can be opened in System Profiler.app

  -json             generates json output instead of plain text

  -timeout          specifies the maximum time to spend gathering information
                    the default is 180 seconds, 0 means no timeout

  Redirect stderr to /dev/null to suppress progress and error messages.

Examples:

  system_profiler
     Generates a text report with the standard detail level.

  system_profiler -detailLevel mini
     Generates a short report without identifying/personal information.

  system_profiler -listDataTypes
     Shows a list of the available data types.

  system_profiler SPSoftwareDataType SPNetworkDataType
     Generates a text report containing only software and network data.

  system_profiler -xml >MySystem.spx
     Creates a XML file which can be opened by System Profiler.app
```

## Examples

##### Generate a short report containing no personal information

```bash
system_profiler -detailLevel mini
```

##### Show list of available data types

```bash
system_profiler -listDataTypes
```

##### Create an XML file which can be opened by System Profile.app

```bash
system_profiler -xml > MyReport.spx
```

## References

- [ss64.com - system_profiler](https://ss64.com/osx/system_profiler.html)
