## react-native-view-more-text

A super lightweight plugin to expand/collapse text in React-Native. Truncated text is ended with dotdotdot.

Working on IOS/Android

![ios](https://raw.githubusercontent.com/stefanue/react-native-text-collapse/master/ios.gif)
![android](https://raw.githubusercontent.com/stefanue/react-native-text-collapse/master/android.gif)

### Installation

```
npm install --save react-native-text-collapse 

```

### Usage

- **numberOfLines**(number)(*required): Number of lines to be displayed.
- **renderViewMore**(object): Render view-more component 
- **renderViewLess**(object): Render view-less component 
- **afterCollapse**(func): Callback after collapsing
- **afterExpand**(func): Callback after expanding


```javascript
  import ViewMoreText from 'react-native-text-collapse';
  
  let Example = React.createClass({
    renderViewMore(onPress){
      return(
        <Text onPress={onPress}>View more</Text>
      )
    };
    renderViewLess(onPress){
      return(
        <Text onPress={onPress}>View less</Text>
      )
    };
    render(){
      return(
        <ViewMoreText
          numberOfLines={3}
          renderViewMore={this.renderViewMore}
          renderViewLess={this.renderViewLess}
          textStyle={{textAlign: 'center'}}
        >
          <Text>
            Lorem ipsum dolor sit amet, in quo dolorum ponderum, nam veri molestie constituto eu. Eum enim tantas sadipscing ne, ut omnes malorum nostrum cum. Errem populo qui ne, ea ipsum antiopam definitionem eos.
          </Text>
        </ViewMoreText>
      )
    }
  })

```
