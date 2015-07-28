[![](http://inno-json-parser.googlecode.com/svn/wiki/logo_inno_json_parser.png)](https://code.google.com/p/inno-json-parser/)

## Reference content ##

  * [JSONGetLastError](#JSONGetLastError.md) function - get information about the last occurred error
  * [JSONLoadFromFile](#JSONLoadFromFile.md) function - try to load and parse a JSON content from file
  * [JSONLoadFromString](#JSONLoadFromString.md) function - try to parse a JSON content from string
  * [JSONSaveToFile](#JSONSaveToFile.md) function - save the JSON content to a file
  * [JSONCloseFile](#JSONCloseFile.md) function - close and release JSON content

  * [JSONQueryString](#JSONQueryString.md) function - query string value of a specified object path
  * [JSONQueryBoolean](#JSONQueryBoolean.md) function - query boolean value of a specified object path
  * [JSONQueryInteger](#JSONQueryInteger.md) function - query integer value of a specified object path
  * [JSONQueryDouble](#JSONQueryDouble.md) function - query floating point value of a specified object path

  * [JSONWriteString](#JSONWriteString.md) function - write or create string value of a specified object path
  * [JSONWriteBoolean](#JSONWriteBoolean.md) function - write or create boolean value of a specified object path
  * [JSONWriteInteger](#JSONWriteInteger.md) function - write or create integer value of a specified object path
  * [JSONWriteDouble](#JSONWriteDouble.md) function - write or create floating point value of a specified object path

<br>
<hr />
<h2>JSONGetLastError</h2>

This function is used to obtain the information about the last error that occurred when calling some of the functions of this library. As a result you will get the last internal error code and to the declared DWORD parameter last OS error code.<br>
<br>
<b>Delphi prototype:</b>

<pre><code>function JSONGetLastError(var SysError: DWORD): DWORD; stdcall;</code></pre>

<b>InnoSetup import prototype:</b>

<pre><code>function JSONGetLastError(var SysError: DWORD): DWORD;<br>
external 'JSONGetLastError@files:jsonparser.dll stdcall';</code></pre>

<b>Parameters</b>

<ol><li>SysError [<a href='DWORD.md'>DWORD</a>] - DWORD parameter which receives the last OS error code</li></ol>

<b>Result</b>

The function returns code of the last internal error that occured when calling some of the functions of this library.<br>
<br>
<br>
<hr />
<h2>JSONLoadFromFile</h2>

This function tries to load and parse a JSON content from a specified file.<br>
<br>
<b>Delphi prototype:</b>

<pre><code>function JSONLoadFromFile(FileName: PWideChar): TJSONHandle; stdcall;</code></pre>

<b>InnoSetup import prototype:</b>

<pre><code>function JSONLoadFromFile(FileName: WideString): TJSONHandle;<br>
external 'JSONLoadFromFile@files:jsonparser.dll stdcall';</code></pre>

<b>Parameters</b>

<ol><li>FileName [<a href='WideString.md'>WideString</a>] - absolute path to the file to be loaded and parsed like a JSON content.</li></ol>

<b>Result</b>

If the function succeeds, the return value is an open handle to the JSON parser, INVALID_JSON_HANDLE otherwise. To get extended error information, call <a href='#JSONGetLastError.md'>JSONGetLastError</a>.<br>
<br>
<br>
<hr />
<img src='http://www.aimsedu.ae/images/under_construction.jpg' />