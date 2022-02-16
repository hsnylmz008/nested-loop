# nested-loop
draw triangle with loop

#Function

```php
public function ucgen($number){
        for($a=1; $a<=$number; $a++) {
            for($b=1; $b<=$a; $b++) {
                print "*";
            }
            print "<br>";
        }
}
```
 
 #Controller
``` php
 public function DefaultController{
    $ucgen = $this->ucgen(10);
    return array ('ucgen' => ucgen);
 }
 ```
 
#View Twig
 ```twig
 {% block body %}
    {{ dump(ucgen) }}
 {% endblock %}
```

#Output
 ```
*
**
***
****
*****
******
*******
********
*********
**********
```



 #Function
```php
for($a=1; $a<=10; $a++) {
	for($b=1; $b<=$a; $b++) {
		print "*";	
	}
	print "<br>";
}
for($a<10; $a>=1; $a--) {
	for($b=1; $b<=$a; $b++) {
		print "*";	
	}
	print "<br>";
}
```

#Output
 ```
*
**
***
****
*****
******
*******
********
*********
**********
***********
**********
*********
********
*******
******
*****
****
***
**
*
```
