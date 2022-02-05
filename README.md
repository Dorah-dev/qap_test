## QuickAdminPanel testing

Just a small project for testing and playing with QAP projects
Requirement 1
List of Section edited and files inserted

I have adited the following controller action: Product model commented by writing edited by Dorah. I have added a comment //edited by DorahPhaleng which marks the information added

Added the corresponding Blade view template resources/views/products/index-paging.blade.php inside Products.php. I have added a comment //edited by Dorah Phaleng which marks the information added

To make the indexPaging() action work, you need to add a route for it to your routes/web.php file: I have added a comment //edited by DorahPhaleng which marks the information added

Requirement 2
I have edited view file,commented with edited by Dorah Phaleng requirement 2
I have edited routes file
I have edited ProductsController,commented with edited by Dorah Phaleng requirement 2

Requirement 3

Then for your showCategory function, you would need something like this:
public function showCategory($id) {
    $category = Categories::find($id);

    // i used categories.show here, change it to whatever view you use
    return view('categories.show')->with('category', $category);
}
Then in your categories.show view, you can access the properties of the category like so:
$category->id; // or whatever you want to display
________________________________________
As per OP's request: the first 5 categories in the database that lead to their pages:
________________________________________
In your controller:
public function myFunction()
{
   $categories = Categories::all()->take(5)->get();

   return view('your.view')->with('categories', $categories);
}
In your blade view (assuming that the view for the category is at: /category/id):
@foreach($categories as $category)
   <a href="/category/{{$category->id}}">{{$category->name}}</a>
@endforeach



Optional requirement 4

I have added another file resources/views/cart.blade.php
I have added  another file resources/views/products.blade.php
I have added another file resources/views/layout.blade.php
 I have added following code on that file:
app/Http/Controllers/ProductController.php

 I have create some routes for add to cart function.

routes/web.php

I have created a seeder
php artisan make:seed ProductSeeder
database/seeders/ProductSeeder.php

I have Created Model

php artisan make:model Product
app/Models/Products.php



I have created migration 
php artisan make:migration create_products_table

I have added public/css/style.css


