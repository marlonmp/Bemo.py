# **Documentaci贸n de los comandos de Bemo** 馃

A continuaci贸n, se presentan los comandos del Bot de m煤sica `Bemo`, con sus respectivos par谩metros y explicaci贸n sencilla de su funcionamiento, estos comandos est谩n divididos en tres secciones:

- **Comandos del canal de voz:** estos comandos ar谩n que Bemo interact煤e con los canales de audio, y los miembros del gremio de Discord.

- **Comandos de lista de m煤sica:** Estos comandos servir谩n para manejar la informaci贸n de las listas de reproducci贸n guardadas en cach茅.

- **Comandos de reproducci贸n:** Estos comandos se encargar谩n de la reproducci贸n de la m煤sica y las listas de reproducci贸n.

## **Par谩metros** 馃搼

- <a name=Id></a> **`Id`:** El par谩metro `Id` es el identificador de una canci贸n o de una lista de reproducci贸n, el id m铆nimo posible es 1. su expresi贸n regular de validaci贸n es: `^\d+$`.

- <a name=Title></a> **`T铆tulo`:** El par谩metro `T铆tulo` hace referencia al t铆tulo de la lista de reproducci贸n, este par谩metro solo puede contener letras de la `a` a la `z` en min煤sculas, guion `-`, guion bajo `_` y n煤meros del `0` al `9`. El t铆tulo solo puede contener entre `3` y `20` caracteres. Su expresi贸n regular de validaci贸n es: `^[a-z\d\-\_]{3,20}$`.

- <a name=Prefix></a> **`Prefijo`:** El par谩metro `Prefijo` es la id o las iniciales del t铆tulo de la lista de reproducci贸n (3 iniciales como m铆nimo). Sus expresiones regulares de validaci贸n son: `^\d+$` o `^[a-z\d\-\_]{3,20}$`.

- <a name=Url></a> **`Url`:** El par谩metro `Url` hace referencia a la direcci贸n (por el momento solo de Youtube) de la canci贸n.

> **Nota:** En todos los comandos que se requiere los par谩metros de la canci贸n y la lista de reproducci贸n, siempre ir谩 primero la informaci贸n de la lista de reproducci贸n y luego la informaci贸n de la canci贸n.

**Comandos del canal de voz** 馃攰
---

> - `!join` : Bemo entrar谩 al canal de voz donde se aloje el emisor del comando.
> 
> - `!link` : Bemo segui谩a al usuario por los canales de voz.
>
> - `!unlink` : Bemo dejar谩 de seguir al usuario enlazado.
>
> - `!leave` : Bemos saldr谩 del canal de voz donde est茅.


**Comandos de m煤sica** 馃幎
---

> - `!show` : Bemo listar谩 todas las listas de reproducci贸n en la cach茅.
>
> - `!list` [`Prefijo`](#Prefix) : Bemo listar谩 las canciones que est茅n en la lista de reproducci贸n seleccionada.
>
> - `!new` [`T铆tulo`](#Title) : Bemo crear谩 una nueva lista de reproducci贸n en cach茅, si el t铆tulo no est谩 en uso.
>
> - `!update` [`Prefijo`](#Prefix) [`Nuevo t铆tulo`](#Title) : Bemo actualizar谩 en cach茅 el t铆tulo de la lista de reproducci贸n seleccionada.
>
> - `!delete` [`Id`](#Id) : Bemo eliminar谩 de al cach茅 la lista de reproducci贸n seleccionada.
>   
> - `!add` [`Prefijo`](#Prefix) [`url`](#Url) : Bemo a帽adir谩 a la lista de reproducci贸n en cach茅 seleccionada la canci贸n de la url.
>
> - `!remove` [`Prefijo`](#Prefix) [`Id`](#Id) : Bemo eliminar谩 del a cach茅 la canci贸n de la lista de reproducci贸n seleccionada.
>
> - `!save` : Bemo guardar谩 en la base de datos la informaci贸n que est茅 en cach茅.
    
**Comandos de reproducci贸n** 鈴?
---

> - `!start` [`Prefijo`](#Prefix) [`opcional[Id]`](#Id) : Si Bemo est谩 en un canal de voz, iniciar谩 la lista de reproducci贸n con la primera canci贸n, o la canci贸n seleccionada.
>    
> - `!play` [`Id`](#Id) : Si Bemo est谩 en un canal, y hay una lista de reproducci贸n iniciada, reproducir谩 la canci贸n indicada en el comando.
>
> - `!replay` : Si Bemo est谩 en un canal, y hay una lista de reproducci贸n iniciada, reiniciar谩 la canci贸n que est谩 sonando.
>
> - `!next` : Si Bemo est谩 en un canal, y hay una lista de reproducci贸n iniciada, reproducir谩 la canci贸n que sigue.  
>
> - `!previus` : Si Bemo est谩 en un canal, y hay una lista de reproducci贸n iniciada, reproducir谩 la canci贸n anterior.
>
> - `!pause` : Si Bemo est谩 en un canal, y hay una lista de reproducci贸n iniciada, pausar谩 la canci贸n que est谩 sonando.
>
> - `!resume` : Si Bemo est谩 en un canal, y hay una lista de reproducci贸n iniciada, y hay m煤sica pausada, la reanudar谩.
>
> - ~~`!loop`~~
>
> - `!shuffle` : Bemo revolver谩 la lista de reproducci贸n iniciada.
  