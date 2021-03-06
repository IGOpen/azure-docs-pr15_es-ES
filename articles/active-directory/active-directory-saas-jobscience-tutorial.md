<properties 
    pageTitle="Tutorial: Integración de Azure Active Directory con Jobscience | Microsoft Azure" 
    description="Aprenda a usar Jobscience con Azure Active Directory para habilitar el inicio de sesión único, aprovisionamiento automatizado y mucho más." 
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

#<a name="tutorial-azure-active-directory-integration-with-jobscience"></a>Tutorial: Integración de Azure Active Directory con Jobscience
  
El objetivo de este tutorial es mostrar la integración de Azure y Jobscience.  
El escenario descrito en este tutorial se supone que ya tiene los siguientes elementos:

-   Una suscripción válida de Azure
-   Una suscripción Jobscience inicio de sesión único habilitado
  
Después de completar este tutorial, los usuarios de Azure AD que ha asignado a Jobscience será capaz de inicio de sesión único en la aplicación en el sitio de su empresa de Jobscience (servicio proveedor inicia sesión) o mediante la [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).
  
El escenario descrito en este tutorial se compone de los siguientes bloques de creación:

1.  Habilitar la integración de aplicación para Jobscience
2.  Configuración de inicio de sesión único
3.  Configuración de aprovisionamiento de usuario
4.  Asignación de usuarios

![Escenario] (./media/active-directory-saas-jobscience-tutorial/IC784341.png "Escenario")
##<a name="enabling-the-application-integration-for-jobscience"></a>Habilitar la integración de aplicación para Jobscience
  
El objetivo de esta sección es describen cómo habilitar la integración de aplicación para Jobscience.

###<a name="to-enable-the-application-integration-for-jobscience-perform-the-following-steps"></a>Para habilitar la integración de aplicación para Jobscience, siga estos pasos:

1.  En el portal de clásico Azure, en el panel de navegación izquierdo, haga clic en **Active Directory**.

    ![Active Directory] (./media/active-directory-saas-jobscience-tutorial/IC700993.png "Active Directory")

2.  En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3.  Para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Aplicaciones] (./media/active-directory-saas-jobscience-tutorial/IC700994.png "Aplicaciones")

4.  Haga clic en **Agregar** en la parte inferior de la página.

    ![Agregar aplicación] (./media/active-directory-saas-jobscience-tutorial/IC749321.png "Agregar aplicación")

5.  En el cuadro de diálogo **¿Qué desea hacer** , haga clic en **Agregar una aplicación de la Galería**.

    ![Agregar una aplicación de gallerry] (./media/active-directory-saas-jobscience-tutorial/IC749322.png "Agregar una aplicación de gallerry")

6.  En el **cuadro de búsqueda**, escriba **jobscience**.

    ![Galería de aplicación] (./media/active-directory-saas-jobscience-tutorial/IC784342.png "Galería de aplicación")

7.  En el panel de resultados, seleccione **Jobscience**y, a continuación, haga clic en **completado** para agregar la aplicación.

    ![Jobscience] (./media/active-directory-saas-jobscience-tutorial/IC784357.png "Jobscience")
##<a name="configuring-single-sign-on"></a>Configuración de inicio de sesión único
  
El objetivo de esta sección es describen cómo habilitar los usuarios autenticar a Jobscience con su cuenta de Azure AD mediante federación basada en el protocolo SAML.  
Configuración de inicio de sesión único para Jobscience requiere que recuperar un valor de la huella digital de un certificado.  
Si no está familiarizado con este procedimiento, consulte [cómo recuperar el valor de la huella digital de un certificado](http://youtu.be/YKQF266SAxI).

###<a name="to-configure-single-sign-on-perform-the-following-steps"></a>Para configurar el inicio de sesión único, realice los pasos siguientes:

1.  Inicie sesión como administrador en el sitio de su empresa Jobscience.

2.  Vaya a **configuración**.

    ![Programa de instalación] (./media/active-directory-saas-jobscience-tutorial/IC784358.png "Programa de instalación")

3.  En el panel de navegación izquierdo, en la sección **Administrar** , haga clic en **Administración de dominios** para expandir la sección relacionada y, a continuación, haga clic en **Mi dominio** para abrir la página de **Mi dominio** . 

    ![Mi dominio] (./media/active-directory-saas-jobscience-tutorial/IC767825.png "Mi dominio")

4.  Para comprobar que su dominio ha sido correctamente el programa de instalación, asegúrese de que se encuentra en "**Paso 4 implementado a los usuarios**" y revise la "**Configuración de mi dominio**".

    ![Dominios implementan al usuario] (./media/active-directory-saas-jobscience-tutorial/IC784377.png "Dominios implementan al usuario")

5.  En una ventana de explorador web diferente, inicie sesión en su portal clásica Azure.

6.  En la página de integración de aplicación **Jobscience** , haga clic en **configurar inicio de sesión único** para abrir el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-jobscience-tutorial/IC784360.png "Configurar el inicio de sesión único")

7.  En la página **¿cómo desea que los usuarios para iniciar sesión Jobscience** , seleccione **Inicio de sesión único de Microsoft Azure AD**y, a continuación, haga clic en **siguiente**.

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-jobscience-tutorial/IC784361.png "Configurar el inicio de sesión único")

8.  En la página **Configurar la dirección URL de aplicación** , en el cuadro de texto **Jobscience inicio de sesión en la URL** , escriba la dirección URL con el siguiente patrón "*http://company.my.salesforce.com*" y, a continuación, haga clic en **siguiente**.

    ![Configurar la dirección URL de la aplicación] (./media/active-directory-saas-jobscience-tutorial/IC784362.png "Configurar la dirección URL de la aplicación")

9.  En la página **configurar inicio de sesión único en Jobscience** , para descargar el certificado, haga clic en **Descargar certificado**y, a continuación, guarde el archivo de certificado localmente en el equipo.

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-jobscience-tutorial/IC784363.png "Configurar el inicio de sesión único")

10. En el sitio de empresa Jobscience, haga clic en **Controles de seguridad**y, a continuación, haga clic en **Configuración de inicio de sesión único**.

    ![Controles de seguridad] (./media/active-directory-saas-jobscience-tutorial/IC784364.png "Controles de seguridad")

11. En la sección **Configuración de inicio de sesión único** , realice los pasos siguientes:

    ![Configuración de inicio de sesión único] (./media/active-directory-saas-jobscience-tutorial/IC781026.png "Configuración de inicio de sesión único")

    1.  Seleccione **SAML habilitado**.
    2.  Haga clic en **nuevo**.

12. En el cuadro de diálogo **SAML solo inicio de sesión en configuración de editar** , realice los pasos siguientes:

    ![Configuración de inicio de sesión único de SAML] (./media/active-directory-saas-jobscience-tutorial/IC784365.png "Configuración de inicio de sesión único de SAML")

    1.  En el cuadro de texto **nombre** , escriba un nombre para la configuración.
    2.  En el portal de clásico Azure, en la página de cuadro de diálogo **configurar inicio de sesión único en Jobscience** , copie el valor de **Dirección URL del emisor** y péguelo en el cuadro de texto del **emisor**
    3.  En el cuadro de texto **Id. de entidad** , escriba **https://salesforce-jobscience.com**
    4.  Haga clic en **Examinar** para cargar el certificado de Azure AD.
    5.  Como **Tipo de identidad de SAML**, seleccione **aserción contiene el identificador de la federación desde el objeto de usuario**.
    6.  Como **Ubicación de identidades SAML**, seleccione **identidad está en el elemento NameIdentfier de la instrucción de asunto**.
    7.  En el portal de clásico Azure, en la página de cuadro de diálogo **configurar inicio de sesión único en Jobscience** , copie el valor de **Dirección URL de inicio de sesión remota** y péguelo en el cuadro de texto **Dirección URL de inicio de sesión del proveedor de identidades**
    8.  En el portal de clásico Azure, en la página de cuadro de diálogo **configurar inicio de sesión único en Jobscience** , copie el valor de **Dirección URL de cierre de sesión remota** y péguelo en el cuadro de texto **Dirección URL de cierre de sesión del proveedor de identidades**
    9.  Haga clic en **Guardar**.

13. En el panel de navegación izquierdo, en la sección **Administrar** , haga clic en **Administración de dominios** para expandir la sección relacionada y, a continuación, haga clic en **Mi dominio** para abrir la página de **Mi dominio** . 

    ![Mi dominio] (./media/active-directory-saas-jobscience-tutorial/IC767825.png "Mi dominio")

14. En la página **Mi dominio** , en la sección **Personalización de marca de página de inicio de sesión** , haga clic en **Editar**.

    ![Página de inicio de sesión de marca] (./media/active-directory-saas-jobscience-tutorial/IC767826.png "Página de inicio de sesión de marca")

15. En la página de **Personalización de marca de página de inicio de sesión** , en la sección **Servicio de autenticación** , se muestra el nombre de la **Configuración de SSO de SAML** . Selecciónelo y, a continuación, haga clic en **Guardar**.

    ![Página de inicio de sesión de marca] (./media/active-directory-saas-jobscience-tutorial/IC784366.png "Página de inicio de sesión de marca")

16. En el portal de clásico Azure, seleccione la confirmación de la configuración de inicio de sesión único y, a continuación, haga clic en **completado** para cerrar el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar el inicio de sesión único] (./media/active-directory-saas-jobscience-tutorial/IC784367.png "Configurar el inicio de sesión único")
  
Para obtener el SP iniciado por inicio de sesión único en la dirección URL de inicio de sesión, haga clic en la **configuración de inicio de sesión único** en la sección del menú de **Controles de seguridad** .

![Controles de seguridad] (./media/active-directory-saas-jobscience-tutorial/IC784368.png "Controles de seguridad")
  
Haga clic en el perfil SSO que haya creado en el paso anterior.  
Esta página muestra el inicio de sesión único en la dirección URL para su empresa (por ejemplo, *https://companyname.my.salesforce.com?so=companyid*).
##<a name="configuring-user-provisioning"></a>Configuración de aprovisionamiento de usuario
  
Para permitir que los usuarios de Azure AD iniciar sesión en Jobscience, debe aprovisionar en Jobscience.  
En el caso de Jobscience, aprovisionamiento es una tarea manual.

###<a name="to-configure-user-provisioning-perform-the-following-steps"></a>Para configurar el aprovisionamiento de usuario, siga estos pasos:

1.  Inicie sesión como administrador en el sitio de su empresa **Jobscience** .

2.  Vaya a configuración

    ![Programa de instalación] (./media/active-directory-saas-jobscience-tutorial/IC784358.png "Programa de instalación")

3.  Vaya a **Administrar usuarios \> usuarios**.

    ![Usuarios] (./media/active-directory-saas-jobscience-tutorial/IC784369.png "Usuarios")

4.  Haga clic en **nuevo usuario**.

    ![Todos los usuarios] (./media/active-directory-saas-jobscience-tutorial/IC784370.png "Todos los usuarios")

5.  En el cuadro de diálogo **Editar usuario** , siga estos pasos:

    ![Editar usuarios] (./media/active-directory-saas-jobscience-tutorial/IC784371.png "Editar usuarios")

    1.  Escriba el nombre, apellido, alias, correo electrónico, las propiedades de nombre y alias de usuario del usuario de Azure AD que desee aprovisionar en los cuadros de texto relacionados.
    2.  Haga clic en **Guardar**.

    >[AZURE.NOTE] Titular de la cuenta de Azure AD recibirá un correo electrónico que incluye un vínculo para confirmar la cuenta antes de que se activa.

>[AZURE.NOTE] Puede usar cualquier otros Jobscience usuario cuenta herramientas de creación o API proporcionan por Jobscience a cuentas de usuario AAD de aprovisionamiento.

##<a name="assigning-users"></a>Asignación de usuarios
  
Para probar la configuración, debe conceder a los usuarios de Azure AD que desea permitir el uso de la aplicación tenga acceso a ella mediante la asignación.

###<a name="to-assign-users-to-jobscience-perform-the-following-steps"></a>Para asignar a los usuarios a Jobscience, siga estos pasos:

1.  En el portal de Azure clásico, cree una cuenta de prueba.

2.  En la página de integración de aplicación **Jobscience **, haga clic en **asignar a los usuarios**.

    ![Asignar usuarios] (./media/active-directory-saas-jobscience-tutorial/IC784372.png "Asignar usuarios")

3.  Seleccione el usuario de prueba, haga clic en **asignar**y, a continuación, haga clic en **Sí** para confirmar la asignación.

    ![Sí] (./media/active-directory-saas-jobscience-tutorial/IC767830.png "Sí")
  
Si desea comprobar la configuración de inicio de sesión único, abra el Panel de acceso. Para obtener más detalles sobre el Panel de acceso, vea [Introducción al Panel de acceso](active-directory-saas-access-panel-introduction.md).