# archie-markup
A Polymer component for parsing ArchieML content.

Parsing element for the [archieml](http://archieml.org/) library. Borrows from Polymer's
`<marked-element>`.

`archie-markup` parses ArchieML content and stores it in its `value` property. This property is
set to notify Polymer of changes. There are a few of ways you can pass ArchieML content.

#### Markup can be passed in using an attribute

```
<archie-markup archieml="[[externalContent]]" value="{{aml}}"></archie-markup>
```

#### Markup can be added as text to the element as well:

```
<archie-markup value="{{aml}}">
  test.one: 1
  test.two: 2
</archie-markup>
```

**Note using the script method is static and the value will not update if the content is changed**

#### An `iron-ajax` element is included and you can make calls with a url attribute

```
<archie-markup url="[[urlToDatafile]]" value="{{aml}}"></archie-markup>
```
