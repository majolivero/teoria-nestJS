# teoria-nestJS

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