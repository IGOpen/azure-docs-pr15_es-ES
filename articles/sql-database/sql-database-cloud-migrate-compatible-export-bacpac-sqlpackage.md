<properties
   pageTitle="Exportar una base de datos de SQL Server a un archivo de MOCHILA con SqlPackage | Microsoft Azure"
   description="Base de datos de Microsoft Azure SQL, migración de base de datos, exportar a base de datos, Exportar archivo MOCHILA, sqlpackage"
   services="sql-database"
   documentationCenter=""
   authors="CarlRabeler"
   manager="jhubbard"
   editor=""/>

<tags
   ms.service="sql-database"
   ms.devlang="NA"
   ms.topic="article"
   ms.tgt_pltfrm="NA"
   ms.workload="sqldb-migrate"
   ms.date="08/24/2016"
   ms.author="carlrab"/>

# <a name="export-a-sql-server-database-to-a-bacpac-file-using-sqlpackage"></a>Exportar una base de datos de SQL Server a un archivo de MOCHILA con SqlPackage

> [AZURE.SELECTOR]
- [SSMS](sql-database-cloud-migrate-compatible-export-bacpac-ssms.md)
- [SqlPackage](sql-database-cloud-migrate-compatible-export-bacpac-sqlpackage.md)

Este artículo le muestra cómo exportar una base de datos de SQL Server a un archivo de [MOCHILA](https://msdn.microsoft.com/library/ee210546.aspx#Anchor_4) mediante la utilidad de línea de comandos de [SqlPackage](https://msdn.microsoft.com/library/hh550080.aspx) . Esta utilidad se incluye con las últimas versiones de [SQL Server Management Studio](https://msdn.microsoft.com/library/mt238290.aspx) y [SQL Server Data Tools para Visual Studio](https://msdn.microsoft.com/library/mt204009.aspx), o puede descargar la versión más reciente de [SqlPackage](https://www.microsoft.com/en-us/download/details.aspx?id=53876) directamente desde el centro de descarga de Microsoft.

1. Abra un símbolo del sistema y cambie un directorio que contiene la utilidad de línea de comandos de sqlpackage.exe: esta herramienta se distribuye con Visual Studio y SQL Server. Use la búsqueda en el equipo para buscar la ruta de acceso en su entorno.
2. Ejecute el siguiente comando sqlpackage.exe con los argumentos siguientes para su entorno:

    ' sqlpackage.exe /Action:Export /ssn: /sdn < nombre_de_servidor >: < database_name > /tf: < target_file >

  	| Argumento  | Descripción  |
  	|---|---|
  	| < nombre_de_servidor >  | nombre del servidor de origen  |
  	| < database_name >  | nombre de la base de datos de origen  |
  	| < target_file >  | nombre de archivo y una ubicación para el archivo de MOCHILA  |

    ![Exportar una aplicación de nivel de datos en el menú de tareas](./media/sql-database-cloud-migrate/TestForCompatibilityUsingSQLPackage01b.png)

## <a name="next-steps"></a>Pasos siguientes

- [Versión más reciente de SSDT](https://msdn.microsoft.com/library/mt204009.aspx)
- [Versión más reciente de SQL Server Management Studio](https://msdn.microsoft.com/library/mt238290.aspx)
- [Importar una MOCHILA a la base de datos de SQL Azure con SSMS](sql-database-cloud-migrate-compatible-import-bacpac-ssms.md)
- [Importar una MOCHILA a SqlPackage de la base de datos SQL Azure](sql-database-cloud-migrate-compatible-import-bacpac-sqlpackage.md)
- [Importar una MOCHILA portal de Azure de base de datos de SQL Azure](sql-database-import.md)
- [Importar una MOCHILA PowerShell de base de datos SQL Azure](sql-database-import-powershell.md)

## <a name="additional-resources"></a>Recursos adicionales

- [V12 de base de datos SQL](sql-database-v12-whats-new.md)
- [Transact-SQL parcialmente o no compatibles de funciones](sql-database-transact-sql-information.md)
- [Migrar las bases de datos no es de SQL Server con el Asistente de migración de SQL Server](http://blogs.msdn.com/b/ssma/)
