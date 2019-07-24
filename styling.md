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

---

React Native uses a cross platform, open source layout library called
[Yoga](https://yogalayout.com/). It implements flexbox.

---

A list of default fonts that are available on each Platform:

[https://github.com/react-native-training/react-native-fonts](https://github.com/react-native-training/react-native-fonts)

---

Conditionally apply styles based on the Platform:

```
import { Platform, StyleSheet } from 'react-native';

StyleSheet.create({
  container: {
    textAlign: 'center',
    ...Platform.select({
      ios: {
        fontFamily: 'American Typewriter'
      },
      android: {
        fontFamily: 'monospace'
      }
    })
  }
});
```
