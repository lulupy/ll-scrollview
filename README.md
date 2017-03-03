# ll-scrollview

基于react的滚动条组件


## 安装

```shell
npm install https://github.com/lulupy/ll-scrollview.git
```

## 使用

```jsx
import React, {Component} from 'react';
import ReactDOM from 'react-dom';
import ScrollView from 'll-scrollview';

import './index.css';

// 到内容高大于容器的高出现竖直滚动条
class Example1 extends Component{
    render(){
        return (
            <ScrollView className="container" style={{width: 200, height: 200}}>
                <div className="inner" style={{ height: 600}}></div>
            </ScrollView>
        )
    }
}

// 到内容宽大于容器的宽出现横向滚动条
class Example2 extends Component{
    render(){
        return (
            <ScrollView className="container" style={{width: 200, height: 200}}>
                <div className="inner" style={{ width: 600,height: 100}}></div>
            </ScrollView>
        )
    }
}


class Example3 extends Component{
    render(){
        return (
            <ScrollView className="container" style={{width: 200, height: 200}}>
                <div className="inner" style={{ width: 600,height: 600}}></div>
            </ScrollView>
        )
    }
}

//当指定了overflow属性， 则根据overflow的属性显示滚动条， 可取值参考css中overflow的取值: auto scroll hidden
class Example4 extends Component{
    render(){
        return (
            <ScrollView className="container" style={{width: 200, height: 200}} overflow="hidden">
                <div className="inner" style={{ width: 600,height: 600}}></div>
            </ScrollView>
        )
    }
}

class Example5 extends Component{
    render(){
        return (
            <ScrollView className="container" style={{width: 200, height: 200}} overflowX="hidden">
                <div className="inner" style={{ width: 600,height: 600}}></div>
            </ScrollView>
        )
    }
}

class Example6 extends Component{
    render(){
        return (
            <ScrollView className="container" style={{width: 200, height: 200}} overflowY="hidden">
                <div className="inner" style={{ width: 600,height: 600}}></div>
            </ScrollView>
        )
    }
}


ReactDOM.render(
    <div>
        <Example1/>
        <Example2/>
        <Example3/>
        <Example4/>
        <Example5/>
        <Example6/>
    </div>,
    document.getElementById('main')
);
```