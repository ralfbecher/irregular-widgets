# irregular-widgets

A Qlik Sense widget library for version 3.1 and later.

## Installation

**Qlik Sense Desktop**

Extract file [bi-irregular-widgets.zip](bi-irregular-widgets.zip) to the extension folder: 

```
C:\Users\<username>\Documents\Qlik\Sense\Extensions
```

**Qlik Sense Server**

Open Qlik Sense QMC on [https://yourserver/qmc](https://yourserver/qmc) and import file [bi-irregular-widgets.zip](bi-irregular-widgets.zip) as extension.

## Widgets

### Dynamic Label Table

A simple table widget (it renders a HTML table and should used for small amounts of data only) providing 20 expression settings for dynamic column labels (headers). You can use any Qlik expression like aggregations and variables. If no expression is set for a label the default label text will be used instead.

For multiple line labels use Qlik function chr(10) as new line: ='Some text' & chr(10) & 'new line..'

![DynamicLabelTable](DynamicLabelTableWidget.png)

**Settings**

![DynamicLabelTable](DynamicLabelTableSettings.png)

Please notice that settings "max. Columns" and "Rows per page" effect the underlaying HyperCube and take place if the Mashup is reloaded (F5).

**Dynamic Coloring**

Extend the measure string with a semicolon + font-color + semicolon + background color:

Use CSS color names:

![DynamicLabelTable](DynamicLabelTableColoring1.png)

Use Qlik color functions:

![DynamicLabelTable](DynamicLabelTableColoring2.png)

If you want to sort by a measure with color coding you need to wrap it into a Dual() function.

**Display Images**

You can encode an image URL and CSS style in the fields data to display images in cells

Syntax of expression:

1. image:
2. URL
3. ;
4. {CSS style JSON}


Example:

```
image:/content/default/logos/logo1.jpg;{'height':10}
```

**Column Sorting**

Column sorting can be changed by click on field label. This works for dimensions and measure.

## Author

**Ralf Becher**

+ [irregular.bi](http://irregular.bi)
* [twitter/irregularbi](http://twitter.com/irregularbi)
* [github.com/ralfbecher](http://github.com/ralfbecher)

## License

Copyright © 2016 Ralf Becher

Released under the MIT license.

***