<properties 
    pageTitle="Tutorial: Integración de Azure Active Directory con SimpleNexus | Microsoft Azure" 
    description="Aprenda a usar SimpleNexus con Azure Active Directory para habilitar el inicio de sesión único, aprovisionamiento automatizado y mucho más." 
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
    ms.date="09/19/2016" 
    ms.author="jeedes" />

#<a name="tutorial-azure-active-directory-integration-with-simplenexus"></a>Tutorial: Integración de Azure Active Directory con SimpleNexus
  
El objetivo de este tutorial es mostrar la integración de Azure y SimpleNexus.  
El escenario descrito en este tutorial se supone que ya tiene los siguientes elementos:

-   Una suscripción válida de Azure
-   Un inicio de sesión único de SimpleNexus activado suscripción
  
Después de completar este tutorial, los usuarios de Azure AD que ha asignado a SimpleNexus será capaz de inicio de sesión único en la aplicación en el sitio de su empresa de SimpleNexus (servicio proveedor inicia sesión) o mediante la [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).
  
El escenario descrito en este tutorial se compone de los siguientes bloques de creación:

1.  Habilitar la integración de aplicación para SimpleNexus
2.  Configuración de inicio de sesión único
3.  Configuración de aprovisionamiento de usuario
4.  Asignación de usuarios

![Escenario] (./media/active-directory-saas-simplenexus-tutorial/IC785893.png "Escenario")
##<a name="enabling-the-application-integration-for-simplenexus"></a>Habilitar la integración de aplicación para SimpleNexus
  
El objetivo de esta sección es describen cómo habilitar la integración de aplicación para SimpleNexus.

###<a name="to-enable-the-application-integration-for-simplenexus-perform-the-following-steps"></a>Para habilitar la integración de aplicación para SimpleNexus, siga estos pasos:

1.  En el portal de clásico Azure, en el panel de navegación izquierdo, haga clic en **Active Directory**.

    ![Active Directory] (./media/active-directory-saas-simplenexus-tutorial/IC700993.png "Active Directory")

2.  En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3.  Para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Aplicaciones] (./media/active-directory-saas-simplenexus-tutorial/IC700994.png "Aplicaciones")

4.  Haga clic en **Agregar** en la parte inferior de la página.

    ![Agregar aplicación] (./media/active-directory-saas-simplenexus-tutorial/IC749321.png "Agregar aplicación")

5.  En el cuadro de diálogo **¿Qué desea hacer** , haga clic en **Agregar una aplicación de la Galería**.

    ![Agregar una aplicación de gallerry] (./media/active-directory-saas-simplenexus-tutorial/IC749322.png "Agregar una aplicación de gallerry")

6.  En el **cuadro de búsqueda**, escriba **nexus simple**.

    ![Galería de aplicación] (./media/active-directory-saas-simplenexus-tutorial/IC785894.png "Galería de aplicación")

7.  En el panel de resultados, seleccione **SimpleNexus**y, a continuación, haga clic en **completado** para agregar la aplicación.

    ![Nexus simple] (./media/active-directory-saas-simplenexus-tutorial/IC809578.png "Nexus simple")
##<a name="configuring-single-sign-on"></a>Configuración de inicio de sesión único
  
El objetivo de esta sección es describen cómo habilitar los usuarios autenticar a SimpleNexus con su cuenta de Azure AD mediante federación basada en el protocolo SAML.

###<a name="to-configure-single-sign-on-perform-the-following-steps"></a>Para configurar el inicio de sesión único, realice los pasos siguientes:

1.  En el portal de clásico Azure, en la página de integración de aplicación **SimpleNexus** , haga clic en **configurar inicio de sesión único** para abrir el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-simplenexus-tutorial/IC785896.png "Configurar el inicio de sesión único")

2.  En la página **¿cómo desea que los usuarios para iniciar sesión SimpleNexus** , seleccione **Inicio de sesión único de Microsoft Azure AD**y, a continuación, haga clic en **siguiente**.

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-simplenexus-tutorial/IC785897.png "Configurar el inicio de sesión único")

3.  En la página **Configurar la dirección URL de aplicación** , en el cuadro de texto **SimpleNexus inicio de sesión en la URL** , escriba la dirección URL con el siguiente patrón "*https://simplenexus.com/CompanyName\_inicio de sesión*" y, a continuación, haga clic en **siguiente**.

    ![Configurar la dirección URL de la aplicación] (./media/active-directory-saas-simplenexus-tutorial/IC786904.png "Configurar la dirección URL de la aplicación")

4.  En la página **configurar inicio de sesión único en SimpleNexus** , haga clic en **descargar metadatos**y, a continuación, reenviar el archivo de metadatos para el equipo de soporte técnico de SimpleNexus.

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-simplenexus-tutorial/IC785899.png "Configurar el inicio de sesión único")

    >[AZURE.NOTE] Inicio de sesión único debe estar habilitado en el equipo de soporte técnico SimpleNexus.

5.  En el portal de clásico Azure, seleccione la confirmación de la configuración de inicio de sesión único y, a continuación, haga clic en **completado** para cerrar el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-simplenexus-tutorial/IC785900.png "Configurar el inicio de sesión único")
##<a name="configuring-user-provisioning"></a>Configuración de aprovisionamiento de usuario
  
Para permitir que los usuarios de Azure AD iniciar sesión en SimpleNexus, debe aprovisionar en SimpleNexus.  
En el caso de SimpleNexus, aprovisionamiento es una tarea manual realizada por el Administrador de inquilinos.

>[AZURE.NOTE] Puede usar cualquier otros SimpleNexus usuario cuenta herramientas de creación o API proporcionan por SimpleNexus a cuentas de usuario AAD de aprovisionamiento.

##<a name="assigning-users"></a>Asignación de usuarios
  
Para probar la configuración, debe conceder a los usuarios de Azure AD que desea permitir el uso de la aplicación tenga acceso a ella mediante la asignación.

###<a name="to-assign-users-to-simplenexus-perform-the-following-steps"></a>Para asignar a los usuarios a SimpleNexus, siga estos pasos:

1.  En el portal de Azure clásico, cree una cuenta de prueba.

2.  En la página de integración de aplicación **SimpleNexus **, haga clic en **asignar a los usuarios**.

    ![Asignar usuarios] (./media/active-directory-saas-simplenexus-tutorial/IC785901.png "Asignar usuarios")

3.  Seleccione el usuario de prueba, haga clic en **asignar**y, a continuación, haga clic en **Sí** para confirmar la asignación.

    ![Sí] (./media/active-directory-saas-simplenexus-tutorial/IC767830.png "Sí")
  
Si desea comprobar la configuración de inicio de sesión único, abra el Panel de acceso. Para obtener más detalles sobre el Panel de acceso, vea [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).