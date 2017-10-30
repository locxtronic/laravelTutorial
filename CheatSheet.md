## Laravel Ultimate Cheat Sheet ##
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

 8. Deleting record <br>
 `$row = ModelName::find($id);` <br>
 `$row->delete();`<br>
 
 9. Generate pagination <br>
`$paginatedModel = ModelName::paginate(offsetValue);` <br>
`$data = ['keyname' => $paginatedModel];`<br>
`return view('viewName', $data);`
 
 10. Error solving for too long column name.
	 11. Goto to folder `app>Providers.`
	 11. Open file AppServiceProvider.php
	 11. Under boot function, paste this code <br>
	`schema::defaultStringLength(191);`
	 11. make sure to <br>
	 `use Illuminate\Support\Facades\schema;`

### Access control ###

 1. Allow access to whole controller if authenticate, using constructor method. <br>
`function __construct() {
	 $this->middleware('auth');
 }`
	
 2. Limiting access for certain function;
 3. Limiting access using route <br>
`Route::get('route','controller@function')>middleware('auth');`
 4. Limiting access in function for authenticated user <br>
`function test() {` <br>
`If (Auth::check()) {`<br>
`// process `<br>
`}` <br>
`}` <br>
	
### Blade ###
 5. Echo variable in view <br>
`{{ $var }}`

 6. Echo full route URL to `<a>` or form `action` <br> and parse value to it. **Only works if route have name.**<br>
`{{ route('controller.function', $var) }}`

 7. Echo the URL of route if the route does not have name. <br>
  `{{ action('controller@function'); }}`

 8. Showing pagination links <br>
`{{ $model->links }}`

 9. Re-display input value in textbox <br>
 `value = "{{ old('elementName') }}"`

 10. Displaying value to textbox from DB or previous inserted value <br>
 `value = "{{ $modelName->attribute or old('elementName') }}"`

