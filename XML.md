## $${\color{red}XML}$$

#### XML Declaration
```xml
<?xml version="1.0" encoding="UTF-8"?>
```

#### Elements
```xml
<element>
  <element2>Content Two</element2> 
  <element3>Content Three</element3>
  <element4/>
</element>
```

#### Attributes
```xml
<element id="666">
  <author level="professional">KENY.STUDIO</author>
</element>
```

#### Content
```xml
<description>My life is <AWESOME> - just joking!</description>
```

#### Comments (Text / PCDATA)
```xml
<!-- Commet Comment -->
```

#### CDATA Section: Character Data.
Blocks of text that are not processed by the parser.<br> Special characters do not need escaping within CDATA.
```xml
<script>
<![CDATA[
  function tryme() {
    if (a < b && c > d) {
      alert("Got it!");
    }
  }
]]>
</script>
```

#### Processing Instructions
```xml
<?xml-stylesheet type="text/css" href="style.css"?>
```

#### Entities
Predefined shortcuts for special characters
```xml
< -> < (Less Than)
> -> > (Greater Than)
& -> & (Ampersand)
' -> ' (Apostrophe / Single Quote)
" -> " (Quotation Mark / Double Quote)
```

#### Namespaces

Avoid naming conflicts when combining elements from different XML vocabularies.
<br> - Default namespace
```xml
<something xmlns="http://example.com/something">
  <author>...</author> <!-- Belongs to http://example.com/something --->
</something>
```
- Prefixed namespace
```xml
<root xmlns:yo="http://example.com/yo" xmlns:nah="http://example.com/nah">
  <yo:book>
    <yo:title>...</yo:title>
    <nah:author>...</nah:author> <!-- Belongs to http://example.com/nah -->
  </yo:book>
</root>
```
