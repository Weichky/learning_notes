## 基本准备
### 基本类
QApplication`基本程序对象，负责窗口`
```C++
int main(int argc,char* argv[]){
QApplication app(argc,argv);
//do something

return app.exec();//exec()方法一直执行
}
```

QLabel`普通标签`
- setText("`some Texts`")

QLineEdit`输入字符`

QPushButton`按钮`
- setText("`some Texts`")

QHBoxLayout/QVBoxLayout`水平/垂直排版`
- addWidget(`object`)`可以添加控件或者排版`

QWidget`用户界面基类`
- setLayout(`Layout`)`输出排版`
- show()`显示`

### more_info
QMainWindow用于功能丰富的大界面，而QWidget用于展示某信息的小界面

### 设计
Layout`排版`
Spacer`占位`
Button
- Push Button
- Tool Button
- Radio Button`单选`
- check Box`复选`
Item View
Item Widget
Container`容纳控件`
Input Widget
Display Widget

### 信号与槽
QString类 类似 String类

connect()
`谁发出信号 发出什么信号 谁处理信号 怎么处理`

pUi-\>close()方法`直接关闭窗口`

pQProcess-\>start(`program`)

QMessageBox::information(`p处理信号者,"标题","信息"`)

example:
```C++
connect(ui->cmdLineEdit,SIGNAL(returnPressed()),this,SLOT(on_commitButton_clicked()));


connect(ui->cancelButton,&QPushButton::clicked,this,&Widget::on_cancelButton_clicked);

  

    connect(ui->browseButton,&QPushButton::clicked,[this](){

       QMessageBox::information(this,"info","click to browse");

    });
```

```C++
void Widget::on_commitButton_clicked(){
    QString program = ui->cmdLineEdit->text();
    QProcess* myProcess = new QProcess(this);
    myProcess->start(program);
}

void Widget::on_cancelButton_clicked(){
    this->close();
}
```

