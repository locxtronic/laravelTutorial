## Laravel Cheat Sheet ##
### Artisan Command ###
 1. Run php server 
 `php artisan serve`
 
 2. Create migration
`php artisan make:migration migration-name(plural)` 
 
 3. Create model
`php artisan make:model tablename(singular with first character in capital)`
 
 4. Create blank controller 
`php artisan make:controller NameController`
 
 5. Create controller with resource 
`php artisan make:controller NameController --resource --model`

 6. Authentication scaffolding 
`php artisan make:auth`

### Active Record ###

 1. Adding model to controller 
 `use App\ModelName`
 
 2. Adding model in folder to controller
 `use App\FolderName\ModelName`
 
 3. Select * from table 
 `ModelName::all();`
 
 4. Select * from table where 
 `ModelName::where(["columnName" => value])->get();`
 
 5. Insert into table 
 `$var = new ModelName;` 
 `$var->columnName = value;` 
 `$var->save();` 
 
 6. Update using id as reference 
 `$row = ModelName::find($id);` 
 `$row->columnName = value;` 
 `$row->save();`
 
 7. Update using column as reference 
 `$query = ModelName::where(["columnName" => value])->get();` 
`$row = $query[0];` 
`$row->columnName = value` 
`$row->save();`