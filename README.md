## Html Agility Pack


### Usages

#### Parser

1. Load Html From Web

- HtmlWeb.Load method gets an HTML document from an internet resource


##### Example

- The following example loads an Html from the web.

```c#
var html = @"http://html-agility-pack.net/";

HtmlWeb web = new HtmlWeb();

var htmlDoc = web.Load(html);

var node = htmlDoc.DocumentNode.SelectSingleNode("//head/title");

Console.WriteLine("Node Name: " + node.Name + "\n" + node.OuterHtml);
```


2. Load Html From String

#### Example

- The following example loads an Html from the specified string.
```c#
var html = @"<!DOCTYPE html>
<html>
<body>
	<h1>This is <b>bold</b> heading</h1>
	<p>This is <u>underlined</u> paragraph</p>
	<h2>This is <i>italic</i> heading</h2>
</body>
</html> ";

var htmlDoc = new HtmlDocument();
htmlDoc.LoadHtml(html);

var htmlBody = htmlDoc.DocumentNode.SelectSingleNode("//body");

Console.WriteLine(htmlBody.OuterHtml);
```


### Read more document 

`https://html-agility-pack.net/documentationhttps://html-agility-pack.net/documentation`