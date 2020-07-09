# 401-03 Readings

## File and Stream I/O
System.IO allows .NET developers to transfer data to and from storage mediums, IO being input/output.
- Streams are an abstract base class that support reading and writing bytes, and have three fundamental operations: reading, writing and seeking.
- Encoded characters can also be handled by system IO, including reading from streams and writing to them in encoded characters such as binary values, bytes, and strings.
- Async I/O opersations stop the UI thread from being blocked up by the resource intensive operation, some methods include CopyToAsynch, FlushAsync, ReadAsync and WriteAsync.
- System.IO.Compression allows for managing compression of files for storage such as zipping them.
- Isolated storage is a "mechanism that provides isolation and safety by defining standardized ways of associating code with saved data. The storage provides a virtual file system that is isolated by user, assembly, and (optionally) domain."

## Write to a file
- StreamWriter contains methods like Write and WriteLine as well as asyncs such as WriteAsync and WriteLineAsync
- File provides static methods for writting text to a file such as WriteAllLiunes and WriteAllText.
- Path is for strings with file or path information, includes the Combine, Join and TryJoin methods.

## Read to a file
"The System.IO.BinaryWriter and System.IO.BinaryReader classes are used for writing and reading data other than character strings. The following example shows how to create an empty file stream, write data to it, and read data from it."