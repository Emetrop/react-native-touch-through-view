# react-native-touch-through-view [![npm version](https://img.shields.io/npm/v/react-native-touch-through-view.svg?style=flat)](https://www.npmjs.com/package/react-native-touch-through-view)

React Native Touch Through View is a simple component library that allows for
scroll views and table views to scroll over interactable content without poor
performing size and bounds animations.

You can achieve Spotify or Apple maps style drawer effects with the full
performance of UIScrollView and without laggy onScroll events.

![Spotify style](http://i.imgur.com/5LaZvUQ.gif)
![Maps style](http://i.imgur.com/sfFI5CA.gif)

## Installation
Simply use `react-native link react-native-touch-through-view` to add the library
to your project.

## How to use it
1. Import the library `import { TouchThroughView, TouchThroughWrapper } from 'react-native-touch-through-view';`
1. Wrap your ListView or ScrollView in the `<TouchThroughWrapper>` element.
1. Add `<TouchThroughView />` elements wherever you want the users touch to be passed through to the view behind. You can style these views just like any other view and put them anywhere in the view you want.

eg.
```javascript
// Markup for listview with a touch through header.
<TouchThroughWrapper style={styles.scrollWrapper}>
      <ListView
        style={styles.scroller}
        dataSource={dataSource}
        renderHeader={() => <TouchThroughView style={styles.touchThroughView} />}
        renderRow={(rowData) => {
          return (
              <View style={styles.itemRow}>
                <Text>{rowData}</Text>
              </View>
          )
        }}>
      </ListView>
    </TouchThroughWrapper>
```

Have a look at the demo in the example directory if you need more help.

## Issues
Currently we are working through an issue at #8 with Android devices on that latest version of React Native not properly passing through touch events. 

## Credits
Brought to you by the team at [Rome2rio](https://www.rome2rio.com). Find out how to join our team at <https://www.rome2rio.com/careers/>
