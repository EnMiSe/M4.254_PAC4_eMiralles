Exercici 2

1. Quina ordre has d'utilitzar per crear un nou projecte Angular utilitzant
Angular CLI anomenat ecommerce?

- ng new ecommerce

Després de llançar aquest comandament, Angular CLI et fa algunes preguntes sobre les característiques del projecte, com  quins estils es volen utilitzar. 

Estructura i Fitxers Generats per Angular CLI
Quan Angular CLI ha acabat de crear el projecte ecommerce, es genera la següent estructura de fitxers i directoris:

- Fitxers de Configuració a l'Arrel del Projecte:

tsconfig.app.json: Conté les opcions de compilació de TypeScript per a l'aplicació.
angular.json: Fitxer de configuració principal per a Angular CLI. Especifica les opcions de construcció, desenvolupament, i proves.

package.json: Enumera les dependències del projecte i els scripts utilitzables.
.editorconfig: Proporciona configuracions d'estil de codi per diferents editors i IDEs.

.gitignore: Especifica els fitxers i directoris que han de ser ignorats per Git.
Directori node_modules
Aquest directori conté totes les llibreries i dependències necessàries per a l'aplicació, especificades en package.json.

- Directori src

index.html: És el fitxer HTML principal on s'executa l'aplicació.
main.ts: El punt d'entrada principal per a l'aplicació Angular. Bootstrap l'aplicació.

styles.css: Fitxer global per als estils CSS de l'aplicació.
Directori assets: S'utilitza per emmagatzemar arxius estàtics com imatges, fonts, etc.

Directori app: Conté els components, serveis, i altres arxius específics de l'aplicació.

Fitxers app.component.*: Inclou els fitxers per al component principal de l'aplicació (HTML, CSS, i TypeScript).

app.module.ts: El mòdul arrel de l'aplicació que declara els components i importa els mòduls necessaris.

2. Explica cadascun dels següents decoradors generats per Angular
CLI, detallant cadascuna de les propietats que es defineixen a:

Els decoradors en Angular són funcions especials que afegeixen metadades a classes, atributs, mètodes o paràmetres. Són fonamentals en el funcionament d'Angular.

### `app.module.ts` - @NgModule

El decorador `@NgModule` defineix un mòdul Angular, que és una classe decorada amb `@NgModule`. El mòdul en Angular organitza components, directives, pipes i serveis relacionats, agrupant-los de manera que puguin ser importats per altres mòduls. Les propietats més comunes en aquest decorador són:

1. **declarations:** Llista de components, directives i pipes que pertanyen a aquest mòdul. Angular crea una instància compartida d'aquests elements quan són necessaris dins del mòdul.

2. **imports:** Llista de mòduls els quals els exports necessita aquest mòdul. Quan importes altres mòduls, tots els seus components, directives i pipes esdevenen accessibles en aquest mòdul.

3. **providers:** Llista de serveis injectables que aquest mòdul contribueix a la col·lecció global de serveis; poden ser injectats als components, directives, pipes i altres serveis dins del mòdul.

4. **bootstrap:** Llista de components que han de ser carregats quan s'inicia aquest mòdul. Habitualment és l'arrel del component d'aplicació.

### `app.component.ts` - @Component

El decorador `@Component` defineix una classe com un component Angular, el qual és una part clau de l'arquitectura Angular. Un component controla una part de la pantalla (una vista) a través de la seva plantilla associada. Les propietats més comunes en aquest decorador són:

1. **selector:** Un identificador únic que permet incrustar aquest component en una plantilla HTML. Funciona com el nom d'etiqueta HTML per a aquest component.

2. **templateUrl:** El camí cap al fitxer de plantilla HTML per a aquest component. Defineix la vista que aquest component controlarà.

3. **styleUrls:** Un array de camins cap als fitxers CSS que contenen els estils específics per a aquest component. Aquests estils només s'aplicaran al component i no afectaran altres elements de l'aplicació.

Els decoradors `@NgModule` i `@Component` són fonamentals en l'estructuració i organització d'aplicacions Angular, proporcionant un marc clar per a la modularització i encapsulació de funcionalitats.


3. És possible poder injectar el template i els estils en línia d'un
component sense necessitat d'especificar-los a templateUrl, styleUrls? És
recomanable fer-ho?

Sí, és possible injectar el template i els estils en línia en un component Angular sense necessitat d'utilitzar templateUrl i styleUrls. Això es fa utilitzant les propietats template i styles directament en el decorador @Component.

L'ús de templates i estils en línia depèn del context i la mida del component:

Per Components Petits: Per a components petits i simples, utilitzar template i styles en línia pot ser pràctic i convenient, ja que manté tot el codi relacionat amb el component en un sol lloc.

Per Components Grans o Complexos: Per a components més grans o complexos, és millor utilitzar templateUrl i styleUrls. Això ajuda a mantenir el codi més organitzat i facilita la lectura i el manteniment. Separar els templates i estils en fitxers diferents fa que el codi sigui més modular i més fàcil de gestionar, especialment en projectes grans.

Rendiment: No hi ha una diferència significativa de rendiment entre utilitzar estils/templates en línia i externs. Angular processa ambdós de manera eficient.

Manteniment i Reutilització: En projectes grans, separar els templates i estils pot millorar el manteniment i la reutilització del codi. A més, els fitxers separats permeten l'ús de preprocessadors CSS i eines d'edició HTML.