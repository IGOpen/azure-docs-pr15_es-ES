<properties
    pageTitle="Tutorial: Integración de Azure Active Directory con Mixpanel | Microsoft Azure"
    description="Obtenga información sobre cómo configurar el inicio de sesión único entre Azure Active Directory y Mixpanel."
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
    ms.date="10/10/2016"
    ms.author="jeedes"/>


# <a name="tutorial-azure-active-directory-integration-with-mixpanel"></a>Tutorial: Integración de Azure Active Directory con Mixpanel

El objetivo de este tutorial es mostrar cómo integrar Mixpanel con Azure Active Directory (AD Azure).

Integrar Mixpanel con Azure AD proporciona las siguientes ventajas:

- Puede controlar en Azure AD quién tiene acceso a Mixpanel
- Puede habilitar los usuarios automáticamente obtener ha iniciado sesión en Mixpanel (inicio de sesión único) con sus cuentas de Azure AD
- Puede administrar las cuentas en una ubicación central: el portal de clásico de Azure


Si desea conocer más detalles sobre la integración de la aplicación de SaaS con Azure AD, vea [¿Qué es el acceso a la aplicación e inicio de sesión único con Azure Active Directory](active-directory-appssoaccess-whatis.md).

## <a name="prerequisites"></a>Requisitos previos

Para configurar la integración de Azure AD con Mixpanel, necesitará los elementos siguientes:

- Una suscripción de Azure AD
- Un Mixpanel inicio de sesión único de suscripción habilitado


> [AZURE.NOTE] Para probar los pasos de este tutorial, no se recomienda utilizar un entorno de producción.


Para probar los pasos de este tutorial, debería seguir estas recomendaciones:

- No debe utilizar su entorno de producción, a menos que esto es necesario.
- Si no tiene un entorno de prueba de Azure AD, puede obtener un mes de una prueba [aquí](https://azure.microsoft.com/pricing/free-trial/).


## <a name="scenario-description"></a>Descripción del escenario
Es el objetivo de este tutorial para que pueda probar Azure AD inicio de sesión único en un entorno de prueba. 

El escenario descrito en este tutorial se compone de dos bloques de creación:

1. Agregar Mixpanel de la Galería
2. Configurar y probar Azure AD de sesión único


## <a name="adding-mixpanel-from-the-gallery"></a>Agregar Mixpanel de la Galería
Para configurar la integración de Mixpanel en Azure AD, debe agregar Mixpanel desde la galería a la lista de aplicaciones de SaaS administradas.

**Para agregar Mixpanel de la galería, realice los pasos siguientes:**

1. En el **portal de clásica Azure**, en el panel de navegación izquierdo, haga clic en **Active Directory**. 

    ![Active Directory][1]

2. En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3. Para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Aplicaciones][2]

4. Haga clic en **Agregar** en la parte inferior de la página.

    ![Aplicaciones][3]

5. En el cuadro de diálogo **¿Qué desea hacer** , haga clic en **Agregar una aplicación de la Galería**.

    ![Aplicaciones][4]

6. En el cuadro Buscar, escriba **Mixpanel**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_01.png)

7. En el panel de resultados, seleccione **Mixpanel**y, a continuación, haga clic en **completado** para agregar la aplicación.


##  <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Configurar y probar Azure AD de sesión único
El objetivo de esta sección es mostrar cómo configurar y probar el inicio de sesión único Azure AD con Mixpanel en función de un usuario de prueba denominado a "Bárbara Menéndez".

Para que el inicio de sesión único para que funcione, debe saber qué es el usuario equivalente en Mixpanel a un usuario en Azure AD Azure AD. En otras palabras, debe establecerse una relación de vínculo entre un usuario de Azure AD y el usuario relacionado en Mixpanel.

Esta relación de vínculo se establece por asignar el valor del **nombre de usuario** en Azure AD como el valor del **nombre de usuario** en Mixpanel.

Para configurar y probar el inicio de sesión único de Azure AD con Mixpanel, debe completar los siguientes bloques de creación:

1. **[Inicio de sesión único en configurar Azure AD](#configuring-azure-ad-single-single-sign-on)** - para permitir a los usuarios usar esta característica.
2. **[Creación de un anuncio de Azure probar usuario](#creating-an-azure-ad-test-user)** - probar Azure AD inicio de sesión único con Britta Simon.
4. **[Crear un Mixpanel probar usuario](#creating-a-mixpanel-test-user)** - a tiene equivalente de Britta Simon en Mixpanel que está vinculado a la representación de Azure AD de ella.
5. **[Asignación de Azure AD probar usuario](#assigning-the-azure-ad-test-user)** - habilitar Britta Simon usar inicio de sesión único en Azure AD.
5. **[Pruebas de inicio de sesión único](#testing-single-sign-on)** : para comprobar si la configuración funciona.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuración de inicio de sesión único de Azure AD en

El objetivo de esta sección es habilitar inicio de sesión único de Azure AD en el portal de clásico Azure y configurar el inicio de sesión único en la aplicación Mixpanel.



**Para configurar el inicio de sesión único Azure AD con Mixpanel, siga estos pasos:**

1. En el portal de clásico Azure, en la página de integración de aplicación **Mixpanel** , haga clic en **configurar inicio de sesión único** para abrir el cuadro de diálogo **Configurar inicio de sesión único** .

    ![Configurar el inicio de sesión único][6] 

2. En la página **¿cómo desea que los usuarios para iniciar sesión Mixpanel** , seleccione **Azure AD inicio de sesión único**y, a continuación, haga clic en **siguiente**.

    ![Configurar el inicio de sesión único](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_03.png) 

3. En la página de diálogo **Configurar opciones de aplicación** , realice los pasos siguientes:

    ![Configurar el inicio de sesión único](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_04.png) 


    una. En el cuadro de texto de **Inicio de sesión en la dirección URL** , escriba la dirección URL utilizada por los usuarios para el inicio de sesión en la aplicación de Mixpanel mediante el siguiente patrón: **"https://mixpanel.com/login/"**.

    > [AZURE.NOTE] Registre [https://mixpanel.com/register/](https://mixpanel.com/register/) para configurar las credenciales de inicio de sesión y el [equipo de soporte técnico de Mixpanel](mailto:support@Mixpanel.com) para habilitar la configuración de SSO para de inquilinos de contacto. También puede obtener el valor de inicio de sesión en la dirección URL si es necesario desde el equipo de soporte de Mixpanel.

    b. Haga clic en **siguiente**,



4. En la página **configurar inicio de sesión único en Mixpanel** , realice los pasos siguientes:

    ![Configurar el inicio de sesión único](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_05.png) 

    una. Haga clic en **Descargar certificado**y, a continuación, guarde el archivo en su equipo. 

    b. Haga clic en **siguiente**.


5. En una ventana de explorador diferente, inicio de sesión en la aplicación Mixpanel como administrador.
   
6. En la parte inferior de la página, haga clic en el icono **del engranaje** en la esquina izquierda. 

    ![En el inicio de sesión único Mixpanel](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_06.png) 

7. Haga clic en la pestaña **seguridad de Access** y, a continuación, haga clic en **Cambiar configuración**.

    ![Configuración de Mixpanel](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_08.png) 
    
8. En la página de diálogo **cambiar el certificado** , haga clic en **Elegir archivo** para cargar el certificado descargado y, a continuación, haga clic en **siguiente**.

    ![Configuración de Mixpanel](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_09.png) 

9. En el portal de clásico Azure, en la página de diálogo **configurar inicio de sesión único en Mixpanel** , copie el valor de la **URL de servicio de inicio de sesión único** , péguela en el cuadro de texto de dirección URL de autenticación en la página de diálogo **cambiar la dirección URL de autenticación** y, a continuación, haga clic en **siguiente**.
 
    ![Configuración de Mixpanel](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_10.png) 
    
1. Haga clic en **Listo**.


6. En el portal de Azure clásico, seleccione la confirmación de la configuración de inicio de sesión único y, a continuación, haga clic en **siguiente**.

    ![En el inicio de sesión único de Azure AD][10]

7. En la página de **confirmación de inicio de sesión único** , haga clic en **completado**.  
 
    ![En el inicio de sesión único de Azure AD][11]




### <a name="creating-an-azure-ad-test-user"></a>Crear un usuario de prueba de Azure AD
Es el objetivo de esta sección crear un usuario de prueba en el portal de clásico Azure denominado a Britta Simon.
En la lista de usuarios, seleccione **Bárbara Menéndez**.

![Crear usuario de Azure AD][20]

**Para crear un usuario de prueba en Azure AD, realice los pasos siguientes:**

1. En el **portal de clásica Azure**, en el panel de navegación izquierdo, haga clic en **Active Directory**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_09.png) 

2. En la lista de **directorio** , seleccione el directorio para el que desea habilitar la integración de directorios.

3. Para mostrar la lista de usuarios, en el menú de la parte superior, haga clic en **usuarios**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_03.png) 

4. Para abrir el cuadro de diálogo **Agregar usuario** , en la barra de herramientas en la parte inferior, haga clic en **Agregar usuario**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_04.png) 

5. En la página de diálogo **Díganos sobre este usuario** , realice los pasos siguientes:

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_05.png) 

    una. Como tipo de usuario, seleccione Nuevo usuario de su organización.

    b. En el **cuadro de texto**de nombre de usuario, escriba **BrittaSimon**.

    c. Haga clic en **siguiente**.

6.  En la página de diálogo de **Perfil de usuario** , realice los pasos siguientes:

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_06.png) 

    una. En el cuadro de texto **nombre** , escriba **Bárbara**.  

    b. En el último cuadro de texto **Nombre** , tipo, **Simon**.

    c. En el cuadro de texto **Nombre para mostrar** , escriba **Bárbara Menéndez**.

    d. En la lista **función** , seleccione el **usuario**.

    e. Haga clic en **siguiente**.

7. En la página de diálogo **obtener una contraseña temporal** , haga clic en **crear**.

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_07.png) 

8. En la página de diálogo **obtener una contraseña temporal** , realice los pasos siguientes:

    ![Crear un usuario de prueba de Azure AD](./media/active-directory-saas-mixpanel-tutorial/create_aaduser_08.png) 

    una. Anote el valor de la **Nueva contraseña**.

    b. Haga clic en **Finalizar**.   



### <a name="creating-a-mixpanel-test-user"></a>Crear un usuario de prueba Mixpanel

Es el objetivo de esta sección crear un usuario llamado a Britta Simon en Mixpanel. 

1.  Inicio de sesión en el sitio de su empresa Mixpanel como administrador.

2.  En la parte inferior de la página, haga clic en el pequeño botón de engranaje en la esquina izquierda para abrir la ventana de **configuración** .

3.  Haga clic en la pestaña **equipo** .

4. En el cuadro de texto de **integrante de grupo** , escriba dirección de correo electrónico de Bárbara en la Azure.
   
    ![Configuración de Mixpanel](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_11.png) 

4.  Haga clic en **Invitar**. 

El usuario recibirá un correo electrónico para configurar su perfil.


### <a name="assigning-the-azure-ad-test-user"></a>Asignar al usuario de prueba de Azure AD

El objetivo de esta sección es habilitar Britta Simon utilizar un inicio de sesión único Azure al conceder acceso a Mixpanel.

![Asignar usuario][200] 

**Para asignar a Britta Simon a Mixpanel, siga estos pasos:**

1. En el portal de clásico de Azure, para abrir la vista de aplicaciones, en la vista de directorio, haga clic en **aplicaciones** en el menú superior.

    ![Asignar usuario][201] 

2. En la lista de aplicaciones, seleccione **Mixpanel**.

    ![Configurar el inicio de sesión único](./media/active-directory-saas-mixpanel-tutorial/tutorial_mixpanel_50.png) 

1. En el menú de la parte superior, haga clic en **usuarios**.

    ![Asignar usuario][203] 

1. En la lista de usuarios, seleccione **Bárbara Menéndez**.

2. En la barra de herramientas en la parte inferior, haga clic en **asignar**.

    ![Asignar usuario][205]



### <a name="testing-single-sign-on"></a>Pruebas de inicio de sesión único

Es el objetivo de esta sección probar la Azure AD única sesión configuración mediante el Panel de acceso.

Al hacer clic en el mosaico de Mixpanel en el Panel de acceso, debe obtener automáticamente ha iniciado sesión en la aplicación Mixpanel.


## <a name="additional-resources"></a>Recursos adicionales

* [Lista de tutoriales sobre cómo integrar aplicaciones de SaaS con Azure Active Directory](active-directory-saas-tutorial-list.md)
* [¿Qué es el acceso a la aplicación e inicio de sesión único con Azure Active Directory?](active-directory-appssoaccess-whatis.md)


<!--Image references-->

[1]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_04.png

[6]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_05.png
[10]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_06.png
[11]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_07.png
[20]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_201.png
[203]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_203.png
[204]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_204.png
[205]: ./media/active-directory-saas-mixpanel-tutorial/tutorial_general_205.png
