---
order: 0
title:
  zh-CN: 基本
  en-US: Basic
---

````jsx
import { SegmentedControl, WingBlank } from 'antd-mobile';

class SegmentedControlExample extends React.Component {
  onChange = (e) => {
    console.log(`selectedIndex:${e.nativeEvent.selectedSegmentIndex}`);
  }
  onValueChange = (value) => {
    console.log(value);
  }
  render() {
    return (
      <WingBlank size="lg" className="sc-example">
        <p className="sub-title">Simplest</p>
        <SegmentedControl values={['切换一', '切换二']} />

        <p className="sub-title">Disabled</p>
        <SegmentedControl values={['切换一', '切换二']} disabled />

        <p className="sub-title">SelectedIndex</p>
        <SegmentedControl selectedIndex={1} values={['切换一', '切换二', '切换三']} />

        <p className="sub-title">TintColor</p>
        <SegmentedControl
          values={['切换一', '切换二', '切换三']}
          tintColor={'#ff0000'}
          style={{ height: '40px', width: '250px' }}
        />

        <p className="sub-title">onChange/onValueChange</p>
        <SegmentedControl
          values={['切换一', '切换二', '切换三']}
          onChange={this.onChange}
          onValueChange={this.onValueChange}
        />
      </WingBlank>
    );
  }
}

ReactDOM.render(<SegmentedControlExample />, mountNode);
````
````css
.sc-example {
  padding-bottom: 13px;
}
.sub-title {
  color: #888;
  font-size: 14px;
  padding: 30px 0 18px 0;
}
````
