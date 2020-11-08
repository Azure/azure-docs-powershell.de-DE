---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179075"
---
# <span data-ttu-id="9e40a-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="9e40a-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="9e40a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e40a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e40a-103">Erstellt eine neue Datenträgerzuordnung</span><span class="sxs-lookup"><span data-stu-id="9e40a-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="9e40a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e40a-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="9e40a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e40a-105">DESCRIPTION</span></span>
<span data-ttu-id="9e40a-106">Das New-AzMigrateDiskMapping-Cmdlet erstellt eine Zuordnung des Quelldatenträgers, der an den zu migrierenden Server angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="9e40a-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="9e40a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e40a-107">EXAMPLES</span></span>

### <span data-ttu-id="9e40a-108">Beispiel 1: Erstellen von Datenträgern</span><span class="sxs-lookup"><span data-stu-id="9e40a-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="9e40a-109">Abrufen von Datenträger Objekten zum Bereitstellen von Eingaben für New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="9e40a-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="9e40a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e40a-110">PARAMETERS</span></span>

### <span data-ttu-id="9e40a-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="9e40a-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="9e40a-112">Gibt den festgelegten Festplatten-Verschlüsselungs an.</span><span class="sxs-lookup"><span data-stu-id="9e40a-112">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e40a-113">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="9e40a-113">-DiskID</span></span>
<span data-ttu-id="9e40a-114">Gibt die Datenträger-ID des Datenträgers an, der mit dem zu migrierenden gefundenen Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9e40a-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e40a-115">-Disktype</span><span class="sxs-lookup"><span data-stu-id="9e40a-115">-DiskType</span></span>
<span data-ttu-id="9e40a-116">Gibt den Typ der für den Azure VM zu verwendenden Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9e40a-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e40a-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="9e40a-117">-IsOSDisk</span></span>
<span data-ttu-id="9e40a-118">Gibt an, ob der Datenträger das Betriebs System für den zu migrierenden Quellserver enthält.</span><span class="sxs-lookup"><span data-stu-id="9e40a-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e40a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e40a-119">CommonParameters</span></span>
<span data-ttu-id="9e40a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e40a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e40a-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e40a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e40a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e40a-122">INPUTS</span></span>

## <span data-ttu-id="9e40a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e40a-123">OUTPUTS</span></span>

### <span data-ttu-id="9e40a-124">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="9e40a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="9e40a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e40a-125">NOTES</span></span>

<span data-ttu-id="9e40a-126">Aliase</span><span class="sxs-lookup"><span data-stu-id="9e40a-126">ALIASES</span></span>

## <span data-ttu-id="9e40a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e40a-127">RELATED LINKS</span></span>

