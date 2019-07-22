# Styling

Apply several styles at once:

```
<View style={[ styles.thing, styles.thing2 ]} />

const styles = StyleSheet.create({
  thing: {
    color: 'red'
  },
  thing2: {
    marginTop: 20
  }
});
```

Convert a stylesheet object to a JS object:

```
StyleSheet.flatten(styles.thing).color;
```
