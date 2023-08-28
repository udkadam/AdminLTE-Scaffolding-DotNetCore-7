# AdminLTE Template - Scaffolding-DotNetCore-7
These are the Scaffolding templates to generate .NET Core Razor Views For AdminLTE Admin Template.

.NET core's default code generator was using default bootstrap styles etc. For one of the project we are using [AdminLTE](https://adminlte.io/)https://adminlte.io/.

We have many views to be generated - 
Index(List)
Create
Edit
Details
Delete

To achieve objectives, we can change default templates used for scaffolding.  I am using Windows 11 for me default templates path for Visual Stuiod 2022 Enterprise edition is as below - 
C:\Users\<MY USERNAME>\.nuget\packages\microsoft.visualstudio.web.codegenerators.mvc\7.0.9\Templates\ViewGenerator

Note: You may need to change user name and path as per your installation.

Apart from AdminLTE this also performs below additional tasks - 
1] While generating controller it derives from BaseController, like below and also generates required constructor. You may need to change the code as per your needs.
![image](https://github.com/udkadam/AdminLTE-Scaffolding-DotNetCore-7/assets/306496/3ce17fbb-7e6a-4486-a9b9-8dc4cb248d1f)

2] For Select Control - added script to Create and Edit Views

<script>
    $(document).ready(function() {
            $('select').select2();
    });
</script>

3] AdminLTE provides really nice DataTables - used below script to enable datatables feature in all the list pages.
@:<script>
    @:$(function () {
        @:$(".table").DataTable({"responsive": true, "lengthChange": false, "autoWidth": false,"buttons": ["copy", "csv", "excel", "pdf", "print", "colvis"]}).buttons().container().appendTo('#example1_wrapper .col-md-6:eq(0)');      
    @:});
@:</script>



