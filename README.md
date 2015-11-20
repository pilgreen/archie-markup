# archieml-element
A Polymer 1.0 component for parsing ArchieML content.

Element wrapper for the [archieml](http://archieml.org/) library. Borrows from Polymer's
`<marked-element>`.

`archieml-element` parses ArchieML content in a child element with the class `archieml-html`. If you
do not provide this child element, the ArchieML source will be rendered within the component and
cannot be styled.

The ArchieML source can be specified with the archieml attribute:

```
<archieml-element archieml="[[externalContent]]"></archieml-element>
```

You can also provide it using a `<script type="text/archieml">` element child:

```
<archieml-element>
  <div class="archieml-html"></div>
  <script type="text/archieml">
    [items]
    name: one

    name: two
  </script>
</archieml-element>
```
