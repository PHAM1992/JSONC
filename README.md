JSONC
=====
# Update to version 1.6.1

## Background

One of the problems you can have developing rich internet applications (RIA) using Javascript is the amount of data being transported to
and from the server.
When data comes from server, this data could be GZipped, but this is not possible when the big amount of data comes from
the browser to the server.

##### JSONC is born to change the way browser vendors think and become an standard when send information to the server efficiently. 


JSONC has two differents approaches to reduce the size of the amount of data to be transported:

* *JSONC.compress* - Compress JSON objects using a map to reduce the size of the keys in JSON objects.
    * Be careful with this method because it's really impressive if you use it with a JSON with a big amount of data, but it
could be awful if you use it to compress JSON objects with small amount of data because it could increase the final size.
    * The rate compression could variate from 7.5% to 32.81% depending of the type and values of data.

## Examples of compression

#### Example data.js.

    Original - 17331 bytes
    Compressed using JSONC - 16025 bytes
    Compression rate - 7.5%


    Original compressed using gzip.js - 5715 bytes
    Compressed using JSONC using gzip.js - 5761 bytes


    Compression rate from original to compressed using JSONC and gzip.js - 66.76%

#### Example data2.js.

    Original - 19031 bytes
    Compressed using JSONC - 12787 bytes
    Compression rate - 32.81%


    Original compressed using gzip.js - 4279 bytes
    Compressed using JSONC using gzip.js - 4664 bytes


    Compression rate from original to compressed using JSONC and gzip.js - 75.49%

## Next steps
#### Implement the gzip class in different languages (Java, Ruby...)
