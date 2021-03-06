<properties 
    pageTitle="Tutorial: Integración de Azure Active Directory con Bime | Microsoft Azure" 
    description="Aprenda a usar Bime con Azure Active Directory para habilitar el inicio de sesión único, aprovisionamiento automatizado y mucho más." 
    services="active-directory" 
    authors="jeevansd"  
    documentationCenter="na" 
    manager="femila"/>
<tags 
    ms.service="active-directory" 
    ms.devlang="na" 
    ms.topic="article" 
    ms.tgt_pltfrm="na" 
    ms.workload="identity" 
    ms.date="09/29/2016" 
    ms.author="jeedes" />

#<a name="tutorial-azure-active-directory-integration-with-bime"></a>Tutorial: Integración de Azure Active Directory con Bime

El objetivo de este tutorial es mostrar la integración de Azure y Bime.  
El escenario descrito en este tutorial se supone que ya tiene los siguientes elementos:

-   Una suscripción válida de Azure
-   Un inquilino Bime

Después de completar este tutorial, los usuarios de Azure AD que ha asignado a Bime será capaz de inicio de sesión único en la aplicación en el sitio de su empresa de Bime (servicio proveedor inicia sesión) o mediante la [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).

El escenario descrito en este tutorial consta de los siguientes elementos:

1.  Habilitar la integración de aplicación para Bime
2.  Configurar el inicio de sesión único
3.  Configuración de aprovisionamiento de usuario
4.  Asignación de usuarios

![Escenario] (./media/active-directory-saas-bime-tutorial/IC775552.png "Escenario")
##<a name="enabling-the-application-integration-for-bime"></a>Habilitar la integración de aplicación para Bime

El objetivo de esta sección es describen cómo habilitar la integración de aplicación para Bime.

###<a name="to-enable-the-application-integration-for-bime-perform-the-following-steps"></a>Para habilitar la integración de aplicación para Bime, siga estos pasos:

1.  En el portal clásico Azure, en el panel de navegación de la izquierda, haga clic en **Active Directory**.

    ![Active Directory] (./media/active-directory-saas-bime-tutorial/IC700993.png "Active Directory")

2.  En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3.  Para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Aplicaciones] (./media/active-directory-saas-bime-tutorial/IC700994.png "Aplicaciones")

4.  Haga clic en **Agregar** en la parte inferior de la página.

    ![Agregar aplicación] (./media/active-directory-saas-bime-tutorial/IC749321.png "Agregar aplicación")

5.  En el cuadro de diálogo **¿Qué desea hacer** , haga clic en **Agregar una aplicación de la Galería**.

    ![Agregar una aplicación de gallerry] (./media/active-directory-saas-bime-tutorial/IC749322.png "Agregar una aplicación de muestra")

6.  En el **cuadro de búsqueda**, escriba **Bime**.

    ![Galería de aplicación] (./media/active-directory-saas-bime-tutorial/IC775553.png "Galería de aplicación")

7.  En el panel de resultados, seleccione **Bime**y, a continuación, haga clic en **completado** para agregar la aplicación.

    ![Bime] (./media/active-directory-saas-bime-tutorial/IC775554.png "Bime")
##<a name="configuring-single-sign-on"></a>Configurar el inicio de sesión único

El objetivo de esta sección es describen cómo habilitar los usuarios autenticar a Bime con su cuenta de Azure AD mediante federación basada en el protocolo SAML.  
Configuración de inicio de sesión único para Bime requiere que recuperar un valor de la huella digital de un certificado.  
Si no está familiarizado con este procedimiento, consulte [cómo recuperar el valor de la huella digital de un certificado](http://youtu.be/YKQF266SAxI).

###<a name="to-configure-single-sign-on-perform-the-following-steps"></a>Para configurar el inicio de sesión único, realice los pasos siguientes:

1.  En el portal de clásico Azure, en la página de integración de aplicación **Bime** , haga clic en **configurar inicio de sesión único** para abrir el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar inicio de sesión único] (./media/active-directory-saas-bime-tutorial/IC771709.png "Configurar inicio de sesión único")

2.  En la página **¿cómo desea que los usuarios para iniciar sesión Bime** , seleccione **Inicio de sesión único de Microsoft Azure AD**y, a continuación, haga clic en **siguiente**.

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-bime-tutorial/IC775555.png "Configurar el inicio de sesión único")

3.  En la página **Configurar la dirección URL de aplicación** , en el cuadro de texto **Bime inicio de sesión en la URL** , escriba la dirección URL con el siguiente patrón "https://*\<nombre del inquilino\>. Bimeapp.com*"y, a continuación, haga clic en **siguiente**.

    ![Configurar la dirección URL de la aplicación] (./media/active-directory-saas-bime-tutorial/IC775556.png "Configurar la dirección URL de la aplicación")

4.  En la página **configurar inicio de sesión único en Bime** , para descargar el certificado, haga clic en **Descargar certificado**y, a continuación, guarde el archivo de certificado localmente como **c:\\Bime.cer**.

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-bime-tutorial/IC775557.png "Configurar el inicio de sesión único")

5.  En una ventana de explorador web diferente, inicie sesión en el sitio de su empresa Bime como administrador.

6.  En la barra de herramientas, haga clic en **Administrador**y a continuación, **cuenta**.

    ![Administrador] (./media/active-directory-saas-bime-tutorial/IC775558.png "Administrador")

7.  En la página de configuración de cuenta, realice los pasos siguientes:

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-bime-tutorial/IC775559.png "Configurar el inicio de sesión único")

    1.  Seleccione **Habilitar SAML autenticación**.
    2.  En el portal de clásico Azure, en la página de diálogo **configurar inicio de sesión único en Bime** , copie el valor de **Dirección URL de inicio de sesión remota** y, a continuación, péguelo en el cuadro de texto **Dirección URL de inicio de sesión remota** .
    3.  Copie el valor de la **huella digital** del certificado exportado y, a continuación, péguelo en el cuadro de texto de la **Huella digital de certificado** .  

        >[AZURE.TIP] Para obtener más detalles, consulte [cómo recuperar el valor de la huella digital de un certificado](http://youtu.be/YKQF266SAxI)

    4.  Haga clic en **Guardar**.

8.  En el portal de clásico Azure, seleccione la confirmación de la configuración de inicio de sesión único y, a continuación, haga clic en **completado** para cerrar el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-bime-tutorial/IC775560.png "Configurar el inicio de sesión único")
##<a name="configuring-user-provisioning"></a>Configuración de aprovisionamiento de usuario

Para permitir que los usuarios de Azure AD iniciar sesión en Bime, debe aprovisionar en Bime.  
En el caso de Bime, aprovisionamiento es una tarea manual.

###<a name="to-configure-user-provisioning-perform-the-following-steps"></a>Para configurar el aprovisionamiento de usuario, siga estos pasos:

1.  Inicie sesión en su inquilino **Bime** .

2.  En la barra de herramientas, haga clic en **Administrador**y a continuación, **los usuarios**.

    ![Administrador] (./media/active-directory-saas-bime-tutorial/IC775561.png "Administrador")

3.  En la **Lista de usuarios**, haga clic en **Agregar nuevo usuario** ("+").

    ![Usuarios] (./media/active-directory-saas-bime-tutorial/IC775562.png "Usuarios")

4.  En la página de diálogo **Detalles de usuario** , realice los pasos siguientes:

    ![Detalles del usuario] (./media/active-directory-saas-bime-tutorial/IC775563.png "Detalles del usuario")

    1.  Escriba el nombre, apellido, inicio de sesión, correo electrónico de una cuenta AAD válida que desee aprovisionar.
    2.  Haga clic en Guardar.

>[AZURE.NOTE] Puede usar cualquier otros Bime usuario cuenta herramientas de creación o API proporcionan por Bime a cuentas de usuario AAD de aprovisionamiento.

##<a name="assigning-users"></a>Asignación de usuarios

Para probar la configuración, debe conceder a los usuarios de Azure AD que desea permitir el uso de la aplicación tenga acceso a ella mediante la asignación.

###<a name="to-assign-users-to-bime-perform-the-following-steps"></a>Para asignar a los usuarios a Bime, siga estos pasos:

1.  En el portal de Azure clásico, cree una cuenta de prueba.

2.  En la página de integración de aplicación **Bime **, haga clic en **asignar a los usuarios**.

    ![Asignar usuarios] (./media/active-directory-saas-bime-tutorial/IC775564.png "Asignar usuarios")

3.  Seleccione el usuario de prueba, haga clic en **asignar**y, a continuación, haga clic en **Sí** para confirmar la asignación.

    ![Sí] (./media/active-directory-saas-bime-tutorial/IC767830.png "Sí")

Si desea comprobar la configuración de inicio de sesión único, abra el Panel de acceso. Para obtener más detalles sobre el Panel de acceso, vea [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).
