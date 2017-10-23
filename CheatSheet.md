## Laravel Cheat Sheet ##
### Artisan Command ###
 1. Run php server <br>
 `php artisan serve`
 
 2. Create migration <br>
`php artisan make:migration migration-name(plural)` 
 
 3. Create model <br>
`php artisan make:model tablename(singular with first character in capital)`
 
 4. Create blank controller <br>
`php artisan make:controller NameController`
 
 5. Create controller with resource <br>
`php artisan make:controller NameController --resource --model`

 6. Authentication scaffolding <br>
`php artisan make:auth`

### Active Record ###

 1. Adding model to controller <br>
 `use App\ModelName`
 
 2. Adding model in folder to controller<br>
 `use App\FolderName\ModelName`
 
 3. Select * from table <br>
 `ModelName::all();`
 
 4. Select * from table where <br>
 `ModelName::where(["columnName" => value])->get();`
 
 5. Insert into table <br>
 `$var = new ModelName;` <br>
 `$var->columnName = value;` <br>
 `$var->save();` <br>
 
 6. Update using id as reference <br>
 `$row = ModelName::find($id);` <br>
 `$row->columnName = value;` <br>
 `$row->save();`<br>
 
 7. Update using column as reference <br>
 `$query = ModelName::where(["columnName" => value])->get();` <br>
`$row = $query[0];` <br>
`$row->columnName = value` <br>
`$row->save();`<br>

 

