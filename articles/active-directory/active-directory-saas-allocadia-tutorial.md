<properties
    pageTitle="Tutorial: Integración de Azure Active Directory con Allocadia | Microsoft Azure"
    description="Obtenga información sobre cómo configurar el inicio de sesión único entre Azure Active Directory y Allocadia."
    services="active-directory"
    documentationCenter=""
    authors="jeevansd"
    manager="femila"
    editor=""/>

<tags
    ms.service="active-directory"
    ms.workload="identity"
    ms.tgt_pltfrm="na"
    ms.devlang="na"
    ms.topic="article"
    ms.date="09/19/2016"
    ms.author="jeedes"/>


# <a name="tutorial-azure-active-directory-integration-with-allocadia"></a>Tutorial: Integración de Azure Active Directory con Allocadia

En este tutorial, aprenderá a integrar Allocadia con Azure Active Directory (AD Azure).

Integrar Allocadia con Azure AD proporciona las siguientes ventajas:

- Puede controlar en Azure AD quién tiene acceso a Allocadia
- Puede habilitar los usuarios automáticamente obtener ha iniciado sesión en Allocadia (inicio de sesión único) con sus cuentas de Azure AD
- Puede administrar las cuentas en una ubicación central: el portal de clásico de Azure

Si desea conocer más detalles sobre la integración de la aplicación de SaaS con Azure AD, vea [¿Qué es el acceso a la aplicación e inicio de sesión único con Azure Active Directory](active-directory-appssoaccess-whatis.md).

## <a name="prerequisites"></a>Requisitos previos

Para configurar la integración de Azure AD con Allocadia, necesitará los elementos siguientes:

- Una suscripción de Azure AD
- Un Allocadia inicio de sesión único de suscripción habilitado


> [AZURE.NOTE] Para probar los pasos de este tutorial, no se recomienda utilizar un entorno de producción.


Para probar los pasos de este tutorial, debería seguir estas recomendaciones:

- No debe utilizar su entorno de producción, a menos que esto es necesario.
- Si no tiene un entorno de prueba de Azure AD, puede obtener un mes de una prueba [aquí](https://azure.microsoft.com/pricing/free-trial/).


## <a name="scenario-description"></a>Descripción del escenario
En este tutorial, se prueba Azure AD inicio de sesión único en un entorno de prueba. El escenario descrito en este tutorial se compone de dos bloques de creación:

1. Agregar Allocadia de la Galería
2. Configurar y probar Azure AD de sesión único


## <a name="adding-allocadia-from-the-gallery"></a>Agregar Allocadia de la Galería
Para configurar la integración de Allocadia en Azure AD, debe agregar Allocadia desde la galería a la lista de aplicaciones de SaaS administradas.

**Para agregar Allocadia de la galería, realice los pasos siguientes:**

1. En el **portal de clásica Azure**, en el panel de navegación izquierdo, haga clic en **Active Directory**. 

    ![Active Directory][1]

2. En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3. Para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Aplicaciones][2]

4. Haga clic en **Agregar** en la parte inferior de la página.

    ![Aplicaciones][3]

5. En el cuadro de diálogo **¿Qué desea hacer** , haga clic en **Agregar una aplicación de la Galería**.

    ![Aplicaciones][4]

6. En el cuadro Buscar, escriba **Allocadia**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_01.png)

7. En el panel de resultados, seleccione **Allocadia**y, a continuación, haga clic en **completado** para agregar la aplicación.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_06.png)

##  <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Configurar y probar Azure AD de sesión único
En esta sección, configurar y probar el inicio de sesión único Azure AD con Allocadia en función de un usuario de prueba denominado a "Bárbara Menéndez".

Para que el inicio de sesión único para que funcione, debe saber qué es el usuario equivalente en Allocadia a un usuario en Azure AD Azure AD. En otras palabras, debe establecerse una relación de vínculo entre un usuario de Azure AD y el usuario relacionado en Allocadia.
Esta relación de vínculo se establece por asignar el valor del **nombre de usuario** en Azure AD como el valor del **nombre de usuario** en Allocadia.

Para configurar y probar el inicio de sesión único de Azure AD con Allocadia, debe completar los siguientes bloques de creación:

1. **[Inicio de sesión único en configurar Azure AD](#configuring-azure-ad-single-single-sign-on)** - para permitir a los usuarios usar esta característica.
2. **[Creación de un anuncio de Azure probar usuario](#creating-an-azure-ad-test-user)** - probar Azure AD inicio de sesión único con Britta Simon.
4. **[Crear un Allocadia probar usuario](#creating-an-allocadia-test-user)** - a tiene equivalente de Britta Simon en Allocadia que está vinculado a la representación de Azure AD de ella.
5. **[Asignación de Azure AD probar usuario](#assigning-the-azure-ad-test-user)** - habilitar Britta Simon usar inicio de sesión único en Azure AD.
5. **[Pruebas de inicio de sesión único](#testing-single-sign-on)** : para comprobar si la configuración funciona.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuración de inicio de sesión único de Azure AD en

En esta sección, habilitar inicio de sesión único de Azure AD en el portal de clásico y configurar el inicio de sesión único en la aplicación Allocadia.


Aplicación de Allocadia espera las afirmaciones SAML en un formato específico. Configure las siguientes notificaciones para esta aplicación. Puede administrar los valores de estos atributos en la pestaña **"Atrribute"** de la aplicación. La siguiente captura de pantalla muestra un ejemplo de este. 

![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_07.png) 

**Para configurar el inicio de sesión único Azure AD con Hightail, siga estos pasos:**


1. En el portal de clásico Azure, en la página de integración de aplicación **Allocadia** , en el menú de la parte superior, haga clic en **atributos**.

    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_general_80.png) 


2. En el cuadro de diálogo **atributos de token SAML** , para cada fila que se muestra en la tabla siguiente, realice los pasos siguientes:

  	| Nombre del atributo | Valor del atributo |
  	| --- | --- |    
  	| nombre | User.givenName |
  	| apellido  | User.Surname |
  	| Correo electrónico | User.Mail |
    

    una. Haga clic en **Agregar usuario atributo** para abrir el cuadro de diálogo **Agregar usuario Attribure** .

    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_general_81.png) 


    b. En el cuadro de texto **Nombre del atributo isErrorPage** , escriba el nombre del atributo que se muestra de la fila.

    c. En la lista **Valor del atributo** , selsect el valor del atributo se muestra de la fila.

    d. Haga clic en **Finalizar**.  
    

3. En el menú de la parte superior, haga clic en **Inicio rápido**.

    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_general_83.png)  


4. En la página **¿cómo desea que los usuarios para iniciar sesión Allocadia** , seleccione **Azure AD inicio de sesión único**y, a continuación, haga clic en **siguiente**.
    
    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_03.png) 

5. En la página de diálogo **Configurar opciones de aplicación** , siga estos pasos:.

    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_04.png) 

    una. En el cuadro identificador, escriba la dirección URL en el modelo siguiente: para uso del entorno de prueba de la dirección URL como **"https://na2standby.allocadia.com"** y para el entorno de producción use **"https://na2.allocadia.com"**

    b. En la dirección URL de respuesta, escriba la dirección URL en el modelo siguiente: para su uso del entorno de prueba el modelo de dirección URL como **"https://na2standby.allocadia.com/allocadia/saml/SSO"** y para el entorno de producción use **"https://na2.allocadia.com/allocadia/saml/SSO"**


6. En la página **configurar inicio de sesión único en Allocadia** , realice los pasos siguientes:

    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_05.png) 

    una. Haga clic en **descargar metadatos**y, a continuación, guarde el archivo en su equipo.

    b. Haga clic en **siguiente**.


7.  Para obtener el SSO configurado para la aplicación, [Allocadia de soporte](mailTo:support@allocadia.com) técnico de contacto y le ayudará a configurar SSO. Por favor, tenga en cuenta que tendrá que enviar correo electrónico y adjuntar descarga el archivo de metadatos para configurar SSO en el lado de Allocadia.
 
    > [AZURE.NOTE] Asegúrese de que el grupo Allocadia establece el valor del identificador en el entorno de prueba como **"https://na2standby.allocadia.com"** y para el entorno de producción, debe ser: **"https://na2.allocadia.com"**


8. En el portal clásico, seleccione la confirmación de la configuración de inicio de sesión único y, a continuación, haga clic en **siguiente**.
    
    ![En el inicio de sesión único de Azure AD][10]

9. En la página de **confirmación de inicio de sesión único** , haga clic en **completado**.  
    
    ![En el inicio de sesión único de Azure AD][11]



### <a name="creating-an-azure-ad-test-user"></a>Crear un usuario de prueba de Azure AD

En esta sección, creará un usuario de prueba en el portal de clásico denominado a Britta Simon.
En la lista de usuarios, seleccione **Bárbara Menéndez**.

![Crear usuario de Azure AD][20]

**Para crear un usuario de prueba en Azure AD, realice los pasos siguientes:**

1. En el **portal de clásica Azure**, en el panel de navegación izquierdo, haga clic en **Active Directory**.
    
    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_09.png) 

2. En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3. Para mostrar la lista de usuarios, en el menú de la parte superior, haga clic en **usuarios**.
    
    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_03.png) 

4. Para abrir el cuadro de diálogo **Agregar usuario** , en la barra de herramientas en la parte inferior, haga clic en **Agregar usuario**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_04.png) 

5. En la página de diálogo **Díganos sobre este usuario** , realice los pasos siguientes:
 
    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_05.png) 

    una. Como tipo de usuario, seleccione Nuevo usuario de su organización.

    b. En el **cuadro de texto**de nombre de usuario, escriba **BrittaSimon**.

    c. Haga clic en **siguiente**.

6.  En la página de diálogo de **Perfil de usuario** , realice los pasos siguientes:

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_06.png) 

    una. En el cuadro de texto **nombre** , escriba **Bárbara**.  

    b. En el último cuadro de texto **Nombre** , tipo, **Simon**.

    c. En el cuadro de texto **Nombre para mostrar** , escriba **Bárbara Menéndez**.

    d. En la lista **función** , seleccione el **usuario**.

    e. Haga clic en **siguiente**.

7. En la página de diálogo **obtener una contraseña temporal** , haga clic en **crear**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_07.png) 

8. En la página de diálogo **obtener una contraseña temporal** , realice los pasos siguientes:

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-allocadia-tutorial/create_aaduser_08.png) 

    una. Anote el valor de la **Nueva contraseña**.

    b. Haga clic en **Finalizar**.   



### <a name="creating-an-allocadia-test-user"></a>Crear un usuario de prueba Allocadia

En esta sección, creará un usuario llamado a Britta Simon en Allocadia. Soporte de aplicaciones de Allocadia acaba de aprovisionamiento de usuario de tiempo. Si ha configurado las notificaciones como se indicó anteriormente en la sección **[Configuración Azure AD inicio de sesión único](#configuring-azure-ad-single-single-sign-on)** se aprovisionar los usuarios de la aplicación. 


> [AZURE.NOTE] Si necesita crear un usuario de forma manual o por lotes de usuarios, debe ponerse en contacto con el equipo de soporte técnico de Allocadia.


### <a name="assigning-the-azure-ad-test-user"></a>Asignar al usuario de prueba de Azure AD

En esta sección, habilitar Britta Simon utilizar un inicio de sesión único Azure al conceder acceso a Allocadia.

![Asignar usuario][200] 

**Para asignar a Britta Simon a Allocadia, siga estos pasos:**

1. En el portal clásico, para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Asignar usuario][201] 

2. En la lista de aplicaciones, seleccione **Allocadia**.

    ![Configurar el inicio de sesión único](./media/active-directory-saas-allocadia-tutorial/tutorial_allocadia_50.png) 

1. En el menú de la parte superior, haga clic en **usuarios**.

    ![Asignar usuario][203] 

1. En la lista de usuarios, seleccione **Bárbara Menéndez**.

2. En la barra de herramientas en la parte inferior, haga clic en **asignar**.

    ![Asignar usuario][205]


### <a name="testing-single-sign-on"></a>Pruebas de inicio de sesión único

En esta sección, pruebe su Azure AD única sesión configuración mediante el Panel de acceso.
Al hacer clic en el mosaico de Allocadia en el Panel de acceso, debe obtener automáticamente ha iniciado sesión en la aplicación Allocadia.


## <a name="additional-resources"></a>Recursos adicionales

* [Lista de tutoriales sobre cómo integrar aplicaciones de SaaS con Azure Active Directory](active-directory-saas-tutorial-list.md)
* [¿Qué es el acceso a la aplicación e inicio de sesión único con Azure Active Directory?](active-directory-appssoaccess-whatis.md)



<!--Image references-->

[1]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_04.png

[6]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_05.png
[10]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_06.png
[11]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_07.png
[20]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_201.png
[203]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_203.png
[204]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_204.png
[205]: ./media/active-directory-saas-allocadia-tutorial/tutorial_general_205.png
