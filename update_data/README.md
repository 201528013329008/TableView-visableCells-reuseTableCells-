## 数据刷新方法
- 重新刷新屏幕上的所有cell<br>
```objc
[self.tableView reloadData];
```
- 刷新特定行的cell<br>
```objc
[self.tableView reloadRowsAtIndexPaths:@[
        [NSIndexPath indexPathForRow:0 inSection:0],
        [NSIndexPath indexPathForRow:1 inSection:0]
        ]
        withRowAnimation:UITableViewRowAnimationLeft];
```
- 插入特定行数的cell<br>
```objc
[self.tableView insertRowsAtIndexPaths:@[
        [NSIndexPath indexPathForRow:0 inSection:0],
        [NSIndexPath indexPathForRow:1 inSection:0]
        ]
        withRowAnimation:UITableViewRowAnimationLeft];
```
- 删除特定行数的cell<br>
```objc
[self.tableView deleteRowsAtIndexPaths:@[
        [NSIndexPath indexPathForRow:0 inSection:0],
        [NSIndexPath indexPathForRow:1 inSection:0]
        ]
        withRowAnimation:UITableViewRowAnimationLeft];
```

## 数据刷新的原则
- 通过修改模型数据，来修改tableView的展示
    - 先修改模型数据
    - 再调用数据刷新方法
- 不要直接修改cell上面子控件的属性
