# teoria-nestJS

**Que es NestJS**

Nest (NestJS) es un framework para crear aplicaciones escalables y eficientes del lado del servidor en Node.js. Utiliza JavaScript progresivo, está creado con TypeScript y es totalmente compatible con él (pero permite a los desarrolladores codificar en JavaScript puro) y combina elementos de OOP (programación orientada a objetos), FP (programación funcional) y FRP (programación reactiva funcional).

**DEPENDENCIAS**

@nestjs/common:
Descripción: Este paquete contiene la mayoría de las utilidades, decoradores y clases base necesarias para el desarrollo de aplicaciones con NestJS. Aquí se encuentran componentes esenciales como los controladores, servicios, filtros de excepciones, pipes, guards, interceptores, entre otros.
Ejemplos de lo que incluye:
Decoradores: como @Controller(), @Get(), @Post(), @Injectable().
Clases base: como HttpException, ValidationPipe, ParseIntPipe.
Utilidades: como Logger, forwardRef(), ModuleRef.


@nestjs/core:
Descripción: Este es el núcleo de NestJS y proporciona los elementos fundamentales que sustentan el framework. Incluye la lógica para la inyección de dependencias, la creación de módulos, el ciclo de vida de la aplicación, y más.
Ejemplos de lo que incluye:
*Kernel: La infraestructura de NestJS que gestiona la creación y el manejo de aplicaciones modulares.
*Inyección de Dependencias: El motor que gestiona la inyección de dependencias en los diferentes componentes (servicios, controladores, etc.).
*Ciclo de Vida: Hooks como onModuleInit(), onModuleDestroy(), que permiten manejar eventos del ciclo de vida de la aplicación.

@nestjs/platform-express:
Descripción: Este paquete proporciona la integración de NestJS con Express, que es uno de los frameworks de servidor HTTP más populares en Node.js. Si eliges Express como plataforma subyacente (lo cual es la opción por defecto en NestJS), esta dependencia maneja la configuración y la interacción con Express.
Ejemplos de lo que incluye:
*Integración con Express: Permite usar middlewares, manejar solicitudes HTTP, y definir rutas utilizando la infraestructura de Express dentro de una aplicación NestJS.
*Adaptadores: Proporciona el adaptador ExpressAdapter, que es necesario para inicializar la aplicación NestJS con Express.

**Explicación de First-Proyect**

**Carpeta src**

**main.ts** : Archivo donde arranca la aplicación. Iniciar el servidor con npm start.

Podemos usar npm run start:dev para correr la aplicación con el código actualizado. 

**app.module.ts**: Es una especie de código inicial o código raíz que contiene controladores, servicios, etc.
Cada módulo contiene una parte de la aplicación. Una aplicación puede estar conformada por muchos módulos y cada módulo tiene distinta funcionalidad.

Módulo principal de la aplicación
```bash
@Module({
  imports: [],
  controllers: [AppController],
  providers: [AppService],
})
export class AppModule {}
```

**app.controller.ts**:Los controladores son las rutas de nuestro servidor.
Los controladores nos permiten las peticiones que vienen desde las aplicaciones cliente. Por ejemplo; el navegador es un cliente, el envía una petición al servidor y el responde a traves de los controladores.

Si quiero tener más rutas debo crear un nuevo controlador.

Aquí usamos los métodos HTTP.

Lo único que hace el controlador es recibir las peticiones, la lógica la creo en los servicios. 

TENER MUY EN CUENTA QUE CON LOS CONTROLADORES ME COMUNICO CON EL CLIENTE.

**Comando de ayuda** npx nest --help (npx si tengo nest instalado localmente)

**DTO**: Objetos que voy a estar transfiriendo entre aplicaciones (Data Transfer Object).
Este concepto de DTO además de usarlo en controllers también lo uso en services.

**task.service.ts**:  este archivo describe lo que yo puedo empezar a reutilizar en otras partes de mi código. 

**task.module.ts** : es como el índice de toda la parte de task 

**interfaces**: Nos ayuda a crear nuestros propios tipos de datos para ayudarle a TypeScript a resaltar el código.









