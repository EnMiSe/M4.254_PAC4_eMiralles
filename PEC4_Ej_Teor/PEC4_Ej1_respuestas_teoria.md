Exercici 1

#### `ng new`

- **Descripció:** Aquest comandament crea un nou projecte Angular. Genera una estructura de directoris amb tots els fitxers necessaris per començar un projecte, incloent la configuració de TypeScript, Angular, tests, entre altres.
- **Ús:** `ng new nom-projecte` crea un nou projecte amb el nom especificat.

#### `ng generate`

Aquest comandament permet crear diferents entitats dins d'un projecte Angular:

- **Component:** Crea un nou component, que és una classe amb el decorador `@Component`. Els components són els blocs bàsics de construcció en aplicacions Angular.
  - **Ús:** `ng generate component nom-component`

- **Directive:** Genera una nova directiva. Les directives permeten adjuntar comportament a elements del DOM.
  - **Ús:** `ng generate directive nom-directiva`

- **Enum:** Crea una nova enumeració, útil per a definir un conjunt de constants nomenades.
  - **Ús:** `ng generate enum nom-enum`

- **Guard:** Genera un nou guardià, que s'utilitza per controlar l'accés a rutes en l'aplicació.
  - **Ús:** `ng generate guard nom-guardia`

- **Interface:** Crea una nova interfície, útil per a definir tipus personalitzats.
  - **Ús:** `ng generate interface nom-interface`

- **Pipe:** Crea una nova pipe, que s'utilitza per a transformar dades en les plantilles.
  - **Ús:** `ng generate pipe nom-pipe`

- **Service:** Genera un nou servei, una classe amb el decorador `@Injectable`, que s'utilitza per encapsular la lògica de negoci i l'accés a dades.
  - **Ús:** `ng generate service nom-servei`

#### `ng serve`

- **Descripció:** Aquest comandament compila l'aplicació i inicia un servidor de desenvolupament. Permet veure l'aplicació en un navegador, recarregant automàticament quan es fan canvis en el codi.
- **Ús:** `ng serve` obre l'aplicació en `http://localhost:4200` per defecte.

#### `ng test`

- **Descripció:** Executa els tests unitaris en el projecte, utilitzant Karma i Jasmine per defecte.
- **Ús:** `ng test` inicia l'execució dels tests.

#### `ng version`

- **Descripció:** Mostra la versió actual d'Angular CLI i les llibreries relacionades.
- **Ús:** `ng version` proporciona detalls sobre les versions instal·lades.
