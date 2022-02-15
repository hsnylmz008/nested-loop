# nested-loop
draw triangle with loop

#Function

```
public function ucgen($number){
        for($a=1; $a<=$number; $a++) {
            for($b=1; $b<=$a; $b++) {
                print "0";
            }
            print "<br>";
        }
}
```
 
 #Controller
``` 
 public function DefaultController{
    $ucgen = $this->ucgen(15);
    return array ('ucgen' => ucgen);
 }
 ```
 
#View Twig
 ```
 {% block body %}
    {{ dump(ucgen) }}
 {% endblock %}
```
