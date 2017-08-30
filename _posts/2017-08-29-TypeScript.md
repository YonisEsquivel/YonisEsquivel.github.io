---
title: "TypeScript"
layout: post
date: 2017-08-29 19:30
image: /assets/images/ts.png
headerImage: true
tag:
- TypeScript
- JavaScript
- E2015
category: blog
author: yonis
description: Cómo tener TypeScript en nuestra máquina

---
TypeScript es un transpilador creado por Microsoft. En este escribimos Javascript ES2015  y TypeScript lo pasa a Javascript que puede interpretar los navegadores. Además de otras funcionalidades.


## Cómo obtenerlo

Ejecutamos el siguiente comando en consola:
{% highlight js %}
npm install -g typescript
{% endhighlight %}


## Cómo compilarlo

Comando:
{% highlight js %}
tsc fileName.ts
{% endhighlight %}


## Observar todos los cambios de un archivo

Comando:
{% highlight js %}
tsc --watch fileName.ts
{% endhighlight %}


## Veamos su uso en acción

Código escrito en TypeScript (fileName.ts):
{% highlight js %}
let Yonis : number = 3;
let Esquivel : string = "hola";
let Gamarra : any [];

interface User{
	name : string,
	age : number,
	date : string
}

class UserAdd{
	users: User[];
	add ( user : User){
		this.users.push(user);
	}
}

const user = new UserAdd();

let user1 : User = {
	name: 'Yonis',
	age : 30,
	date : '22/08/2017'
}
user.add(user1);
{% endhighlight %}


Luego de compilar, el código final queda así (fileName.js):
{% highlight js %}
var Yonis = 3;
var Esquivel = "hola";
var Gamarra;
var UserAdd = (function () {
    function UserAdd() {
    }
    UserAdd.prototype.add = function (user) {
        this.users.push(user);
    };
    return UserAdd;
}());
var user = new UserAdd();
var user1 = {
    name: 'Yonis',
    age: 30,
    date: '22/08/2017'
};
user.add(user1);
{% endhighlight %}

En el uso díario de este transpilador veremos sus bondades. Podemos además visitar su documentación oficial [AQUí](https://www.typescriptlang.org/docs/home.html).






