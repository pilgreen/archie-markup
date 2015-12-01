# archieml-element
A Polymer 1.0 component for parsing ArchieML content.

Parsing element for the [archieml](http://archieml.org/) library. Borrows from Polymer's
`<marked-element>`.

`archieml-element` parses ArchieML content and stores it in its `value` property. This property is
set to notify Polymer of changes. There are a few of ways you can pass ArchieML content.

#### Archieml content can be passed in using an attribute

```
<archieml-element archieml="[[externalContent]]" value="{{aml}}"></archieml-element>
```

#### Archieml content can be added as a `<script type="text/archieml">` element child:

```
<archieml-element value="{{aml}}">
  <script type="text/archieml">
    [items]
    name: one

    name: two
  </script>
</archieml-element>
```

**Note using the script method is static and the value will not update if the content is changed**

#### An `iron-ajax` element is included and you can make calls with a url attribute

```
<archieml-element url="[[urlToDatafile]]" value="{{aml}}"></archieml-element>
```
