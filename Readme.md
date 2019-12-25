<!-- default file list -->
*Files to look at*:

* [Index.razor](./CS/BlazorProject/Pages/Index.razor)
<!-- default file list end -->

### DataGrid for Blazor - How to create DataGrid and its columns at runtime

This example shows how to create DataGrid components at runtime and create its columns dynamically.
The easiest way to do so is to write a method that returns the **RenderFragment\<T\>** object, for example, in the following manner:
```
RenderFragment<DataItem> buildGridsWithColumns = (dataObject) =>
@<DxDataGrid Data="@dataObject.Data">
    @foreach (var column in dataObject.ColumnNames)
    {
        <DxDataGridColumn Field="@column" />
    }
</DxDataGrid>;
```
The call of such a method creates a grid with columns.
