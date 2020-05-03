---
title: "Info"
categories:
  - testing
tags:
  - literatura
  - poemas
last_modified_at: 2020-05-03T12:25:52-05:00
---

**Cosas un poco raras de laravel** 

Intentando ocultar una relacion que había utilizado para otras cosas

```php
$collection->hidden()
```

@panda20145#7783 parece que para ocultar relaciones de una collecion de modelos (sin tener que hacer un map completo) se tiene que usar el nombre de la relacion, no su nombre estático

En otras palabras
Si tienes un modelo estilo
```php
$users->with('Cards');
```

Y quieres ocultar la propiedad 'Cards' al hacer `->toArray()`, puede uno simplemente hacer un `$users->hide('Cards')`. A pesar de que al hacer `toArray()` el nombre de la coleccion sea 'cards'

