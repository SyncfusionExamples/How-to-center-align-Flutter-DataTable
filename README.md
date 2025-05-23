# How to center align Flutter DataTable (SfDataGrid)?

In this article, we will show how to center-align [Flutter DataTable](https://www.syncfusion.com/flutter-widgets/flutter-datagrid).

Initialize the [SfDataGrid](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/SfDataGrid-class.html) widget with the required properties. By default, the DataGrid occupies the full width and height of its parent widget. To center it within the available space, wrap it in a Center widget and explicitly specify a fixed width and height. This ensures the DataGrid is properly centered on the screen.

```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Syncfusion Flutter DataGrid')),
      body: Center(
        child: SizedBox(
          width: 500,
          height: 550,
          child: SfDataGrid(
            source: employeeDataSource,
            columnWidthMode: ColumnWidthMode.fill,
            columns: <GridColumn>[
              GridColumn(
                columnName: 'id',
                label: Container(
                  padding: EdgeInsets.all(16.0),
                  alignment: Alignment.center,
                  child: Text('ID'),
                ),
              ),
              GridColumn(
                columnName: 'name',
                label: Container(
                  padding: EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: Text('Name'),
                ),
              ),
              GridColumn(
                columnName: 'designation',
                label: Container(
                  padding: EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: Text('Designation', overflow: TextOverflow.ellipsis),
                ),
              ),
              GridColumn(
                columnName: 'salary',
                label: Container(
                  padding: EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: Text('Salary'),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
```

You can download this example on [GitHub]().