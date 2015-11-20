# archieml-element
A Polymer 1.0 component for parsing ArchieML content.

Parsing element for the [archieml](http://archieml.org/) library. Borrows from Polymer's
`<marked-element>`.

`archieml-element` parses ArchieML content and stores it in its `value` property. This property is
set to notify Polymer of changes. There are a couple of ways you can pass ArchieML content.

The ArchieML source can be specified with the archieml attribute:

```
<archieml-element archieml="[[externalContent]]" value="{{aml}}"></archieml-element>
```

You can also provide it using a `<script type="text/archieml">` element child:

```
<archieml-element value="{{aml}}">
  <script type="text/archieml">
    [items]
    name: one

    name: two
  </script>
</archieml-element>
```

**Note using the script method is static and content will not update if the content is changed**
