<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/230140164/19.1.10%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T848300)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
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
