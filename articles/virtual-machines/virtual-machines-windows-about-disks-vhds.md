<properties
    pageTitle="Acerca de discos y VHD para máquinas virtuales de Windows | Microsoft Azure"
    description="Obtenga información sobre los conceptos básicos de los discos y máquinas virtuales VHD para Windows Azure."
    services="virtual-machines-windows"
    documentationCenter=""
    authors="cynthn"
    manager="timlt"
    editor="tysonn"
    tags="azure-resource-manager,azure-service-management"/>

<tags
    ms.service="virtual-machines-windows"
    ms.workload="infrastructure-services"
    ms.tgt_pltfrm="vm-windows"
    ms.devlang="na"
    ms.topic="article"
    ms.date="09/27/2016"
    ms.author="cynthn"/>

# <a name="about-disks-and-vhds-for-azure-virtual-machines"></a>Acerca de discos y VHD para máquinas virtuales de Windows Azure

Al igual que cualquier otro equipo, máquinas virtuales de Azure usar discos como un lugar para almacenar un sistema operativo, aplicaciones y datos. Todos los equipos virtuales Azure tiene al menos dos discos: un sistema operativo Windows y un disco temporal. Crear el disco de sistema operativo de una imagen y el disco de sistema operativo y la imagen son disco duro virtual (VHD) almacenado en una cuenta de almacenamiento de Azure. Máquinas virtuales también pueden tener uno o más discos de datos, que también se almacenan como VHD. En este artículo también está disponible para [máquinas virtuales de Linux](virtual-machines-linux-about-disks-vhds.md).

[AZURE.INCLUDE [learn-about-deployment-models](../../includes/learn-about-deployment-models-both-include.md)]



## <a name="operating-system-disk"></a>Disco del sistema operativo

Cada máquina virtual tiene un disco de sistema operativo acoplado. Tiene registrada como una unidad SATA y marcado como la unidad C: de forma predeterminada. El disco tiene una capacidad máxima de 1023 gigabytes (GB). 

##<a name="temporary-disk"></a>Disco temporal

El disco temporal se creará automáticamente. El disco temporal está etiquetado como la unidad D: de forma predeterminada y se utiliza para almacenar pagefile.sys. 

El tamaño del disco temporal varía según el tamaño de la máquina virtual. Para obtener más información, vea [máquinas virtuales de tamaños para Windows](virtual-machines-windows-sizes.md).

>[AZURE.WARNING] No almacene los datos en el disco temporal. Proporciona almacenamiento temporal para aplicaciones y procesos y pretende sólo almacenar datos como página o intercambiar archivos. Para volver a asignar este disco a una letra de unidad diferente, vea [cambiar la letra del disco temporal de Windows](virtual-machines-windows-classic-change-drive-letter.md).

Para obtener más información sobre cómo Azure usa el disco temporal, consulte [Descripción de la unidad temporal en Microsoft Azure máquinas virtuales de Windows](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)

## <a name="data-disk"></a>Disco de datos

Un disco de datos es un disco duro virtual que está conectado a una máquina virtual para almacenar los datos de la aplicación u otros datos que necesite mantener. Discos de datos se registran como unidades SCSI y están etiquetados con una letra que elija.  Cada disco de datos tiene una capacidad máxima de 1023 GB. El tamaño de la máquina virtual determina cuántos discos de datos que puede adjuntar a ella y el tipo de almacenamiento puede usar para los discos de host.

>[AZURE.NOTE] Para obtener más información sobre las capacidades de máquinas virtuales de Windows, vea [máquinas virtuales de tamaños para Windows](virtual-machines-windows-sizes.md).

Azure crea un disco de sistema operativo cuando se crea una máquina virtual de una imagen. Si usa una imagen que incluya discos de datos, Azure también crea los discos de datos cuando se crea la máquina virtual. En caso contrario, agregar discos de datos después de crear la máquina virtual.

Puede agregar discos de datos a una máquina virtual en cualquier momento, **adjuntando** el disco de la máquina virtual. Puede usar un disco duro virtual que ha cargado o copiado a su cuenta de almacenamiento, o a uno que Azure crea automáticamente. Asociar un disco de datos, asocia el archivo de disco duro virtual con la máquina virtual colocando una concesión de' ' en el disco duro virtual para que no se pueden eliminar de almacenamiento mientras todavía está conectado.

## <a name="about-vhds"></a>Acerca de VHD

Los VHD usados en Azure son archivos .vhd almacenados como blobs de página en una cuenta de almacenamiento estándar o premium en Azure. Para obtener más información acerca de blobs de página, vea [BLOB de bloque de descripción y blobs de página](https://msdn.microsoft.com/library/ee691964.aspx). Para obtener más información sobre el almacenamiento de premium, vea [almacenamiento Premium: almacenamiento de alto rendimiento para cargas de trabajo de Azure máquina virtual](../storage/storage-premium-storage.md).

Azure es compatible con el formato de disco duro virtual fijo de disco. Formato fijo dispone del disco lógico lineal dentro del archivo para que ese desplazamiento de disco X se almacena en el desplazamiento de blob X. Un pequeño pie de página al final del blob describe las propiedades del disco duro virtual. A menudo, los residuos formato fijo de espacio porque la mayoría de los discos tienen grandes rangos sin usar en ellos. Sin embargo, Azure almacena archivos .vhd en un formato disperso, para que reciba las ventajas de los discos fijos y dinámicos al mismo tiempo. Para obtener más información, vea [Introducción a los discos duro virtuales](https://technet.microsoft.com/library/dd979539.aspx).

Todos los archivos .vhd en Azure que desee usar como origen de para crear discos o imágenes son de solo lectura. Cuando se crea una imagen o un disco, Azure hace copias de los archivos .vhd. Estas copias pueden ser de solo lectura o de lectura y escritura, dependiendo de cómo usar el disco duro virtual.

Cuando se crea una máquina virtual de una imagen, Azure crea un disco de la máquina virtual que es una copia del archivo .vhd de origen. Para evitar el borrado accidental, Azure coloca una concesión en cualquier archivo .vhd de origen que se usa para crear una imagen, un disco de sistema operativo o un disco de datos.

Antes de eliminar un archivo .vhd de origen, debe quitar la concesión eliminando el disco o la imagen. Puede eliminar la máquina virtual, el disco de sistema operativo, y el archivo .vhd de origen a la vez eliminando la máquina virtual y todos los eliminar asociados discos. Sin embargo, la eliminación de un archivo .vhd que es un origen de datos de disco requiere varios pasos en un orden del conjunto. Primero desconecte el disco de la máquina virtual, a continuación, eliminar el disco y, a continuación, elimine el archivo .vhd.

>[AZURE.WARNING] Si elimina un archivo .vhd de origen de almacenamiento, o eliminar la cuenta de almacenamiento, Microsoft no puede recuperar los datos por usted.



## <a name="next-steps"></a>Pasos siguientes
-  [Adjuntar un disco](virtual-machines-windows-attach-disk-portal.md) agregar almacenamiento adicional para su máquina virtual.
-  [Cargar una imagen de máquina virtual de Windows Azure](virtual-machines-windows-upload-image.md) al crear una nueva máquina virtual.
-  [Cambiar la letra del disco temporal de Windows](virtual-machines-windows-classic-change-drive-letter.md) para que la aplicación puede utilizar la unidad D: para los datos.
