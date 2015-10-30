# archieml-element
A Polymer 1.0 component for parsing ArchieML content.

`archieml-element` parses [ArchieML](http://archieml.org/) content and notifies Polymer of a change to the value. You can pass initial data inside the element or use the `content` attribute to parse external data from an ajax call (or whatever you like).

### inline example

```
<archie-ml value="{{aml}}">
  [items]
  name: one

  name: two
</archie-ml>
```

### external example

```
<archie-ml content="[[externalContent]] value="{{aml}}"></archie-ml>
```

There are no additional events, but the `value` attribute is set to notify.
