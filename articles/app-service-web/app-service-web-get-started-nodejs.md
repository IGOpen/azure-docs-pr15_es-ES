<properties 
    pageTitle="Implementar la aplicación web de Node.js en Azure de cinco minutos | Microsoft Azure" 
    description="Aprenda lo fácil que es ejecutar aplicaciones web en el servicio de aplicación al implementar una aplicación de ejemplo. Empezar a hacer desarrollo real rápidamente y ver los resultados inmediatamente." 
    services="app-service\web"
    documentationCenter=""
    authors="cephalin"
    manager="wpickett"
    editor=""
/>

<tags
    ms.service="app-service-web"
    ms.workload="web"
    ms.tgt_pltfrm="na"
    ms.devlang="na"
    ms.topic="hero-article"
    ms.date="10/13/2016" 
    ms.author="cephalin"
/>
    
# <a name="deploy-your-first-nodejs-web-app-to-azure-in-five-minutes"></a>Implementar la aplicación web de Node.js primera en Azure de cinco minutos

Este tutorial le ayuda a implementar la primera aplicación web de Node.js al [Servicio de la aplicación de Azure](../app-service/app-service-value-prop-what-is.md).
Puede usar la aplicación de servicio para crear aplicaciones web, [una aplicación móvil extremos](/documentation/learning-paths/appservice-mobileapps/)y [aplicaciones de la API](../app-service-api/app-service-api-apps-why-best-platform.md).

Podrá: 

- Crear una aplicación web en la aplicación de servicio de Azure.
- Implementar un código de ejemplo Node.js.
- Vea el código que se ejecuta live en producción.
- Actualizar la aplicación web de la misma manera que lo haría [inserción que se compromete Git](https://git-scm.com/docs/git-push).

## <a name="prerequisites"></a>Requisitos previos

- [Git](http://www.git-scm.com/downloads).
- [CLI azure](../xplat-cli-install.md).
- Una cuenta de Microsoft Azure. Si no tiene una cuenta, puede [registrarse para una prueba gratuita](/pricing/free-trial/?WT.mc_id=A261C142F) o [activar las ventajas de suscriptor de Visual Studio](/pricing/member-offers/msdn-benefits-details/?WT.mc_id=A261C142F).

>[AZURE.NOTE] Puede [Probar el servicio de aplicación](http://go.microsoft.com/fwlink/?LinkId=523751) sin una cuenta de Azure. Crear una aplicación de inicio y jugar con él para hasta una hora--necesaria ninguna tarjeta de crédito, sin compromisos.

## <a name="deploy-a-nodejs-web-app"></a>Implementar una aplicación web de Node.js

1. Abra un nuevo símbolo de Windows, la ventana de PowerShell, el shell de Linux o el terminal de OS X. Ejecutar `git --version` y `azure --version` para verificar que Git y Azure CLI están instalados en su equipo.

    ![Probar la instalación de herramientas CLI para la aplicación web de primera en Azure](./media/app-service-web-get-started/1-test-tools.png)

    Si no ha instalado las herramientas, vea [requisitos previos](#Prerequisites) para los vínculos de descarga.

3. Inicie sesión en Azure similar a esta:

        azure login

    Seguir el mensaje de ayuda para continuar el proceso de inicio de sesión.

    ![Inicie sesión en Azure para crear su primera aplicación web](./media/app-service-web-get-started/3-azure-login.png)

4. Cambiar CLI de Azure en modo de ASM y a continuación, establezca el usuario de implementación de aplicación de servicio. Va a implementar código usando las credenciales más adelante.

        azure config mode asm
        azure site deployment user set --username <username> --pass <password>

1. Cambiar a un directorio de trabajo (`CD`) y clonar la aplicación de ejemplo similar a esta:

        git clone https://github.com/Azure-Samples/app-service-web-nodejs-get-started.git

2. Cambiar al repositorio de la aplicación de ejemplo.

        cd app-service-web-nodejs-get-started

4. Crear el recurso de la aplicación de servicio de aplicación en Azure con un nombre de aplicación única y el usuario de implementación configurado previamente. Cuando se le solicite, especifique el número de la región que desee.

        azure site create <app_name> --git --gitusername <username>

    ![Crear el recurso de Azure para la primera aplicación web de Azure](./media/app-service-web-get-started-languages/node-site-create.png)

    La aplicación se crea en Azure ahora. Además, el directorio actual es inicializado Git y está conectado a la nueva aplicación de servicio de aplicación como un Git remoto.
    Puede ir a la dirección URL de la aplicación (http://&lt;app_name >. azurewebsites.net) para ver la página HTML bonitas predeterminada, pero vamos a realmente obtener el código ahora.

4. Implementar el código de ejemplo en la aplicación de Azure igual que lleven a cualquier código con Git. Cuando se le pida, escriba la contraseña que configuró anteriormente.

        git push azure master

    ![Código de inserción a la primera aplicación web de Azure](./media/app-service-web-get-started-languages/node-git-push.png)

    `git push`no solo incluye código en Azure, pero también desencadenadores tareas de implementación en el motor de implementación. 
    Si tiene un package.json en la raíz del proyecto (repositorio), el script de implementación restaura los paquetes necesarios para usted. 

Enhorabuena, ha implementado la aplicación de servicio de la aplicación de Azure.

## <a name="see-your-app-running-live"></a>Ver la aplicación que se ejecuta live

Para ver la aplicación ejecutándose en vivo en Azure, ejecute este comando desde cualquier directorio en el repositorio de:

    azure site browse

## <a name="make-updates-to-your-app"></a>Realizar actualizaciones a su aplicación

Ahora puede usar Git insertar desde la raíz de proyecto (repositorio) en cualquier momento para realizar una actualización en el sitio en vivo. Que lo hace la misma manera que cuando se implementa el código de la primera vez. Por ejemplo, cada vez que desea insertar un nuevo cambio que ha probado localmente, simplemente ejecute los comandos siguientes desde la raíz de proyecto (repositorio):

    git add .
    git commit -m "<your_message>"
    git push azure master

## <a name="next-steps"></a>Pasos siguientes

[Crear, configurar e implementar una aplicación web de Node.js Express a Azure](app-service-web-nodejs-get-started.md). Siguiendo este tutorial, aprenderá los conocimientos básicos que necesita para ejecutar cualquier aplicación web de Node.js en Azure, como por ejemplo:

- Crear y configurar aplicaciones en Azure de PowerShell/intensiva.
- Establezca la versión de Node.js.
- Usar un archivo de inicio no está en el directorio raíz de la aplicación.
- Automatizar con NPM.
- Obtener los registros de error y de salida.

O bien, hacer más cosas con su primera aplicación web. Por ejemplo:

- Pruebe [otros modos de implementar código para Azure](../app-service-web/web-sites-deploy.md). Por ejemplo, para implementar desde uno de los repositorios GitHub, simplemente seleccione **GitHub** en lugar de **Repositorio Git Local** en **las opciones de implementación**.
- Llevar su aplicación Azure al siguiente nivel. Autenticar a sus usuarios. Escala que basa a petición. Configurar algunas alertas de rendimiento. Con unos pocos clics. Consulte [Agregar funcionalidad a su primera aplicación web](app-service-web-get-started-2.md).

