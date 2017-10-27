## Access control ##

1. Allow access to whole controller if authenticate, using constructor method.
`function __construct() {
	 $this->middleware('auth');
 }`
	
2. Limiting access for certain function;
- Limiting access using route
`Route::get('route','controller@function')>middleware('auth');`
- Limiting access in function for authenticated user 
`function test() {
 If (Auth::check()) {
	// process 
}
}`
	