---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934003"
---
# <span data-ttu-id="e8a6e-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="e8a6e-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="e8a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a6e-103">Erstellt eine neue Datenträgerzuordnung</span><span class="sxs-lookup"><span data-stu-id="e8a6e-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="e8a6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8a6e-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="e8a6e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8a6e-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a6e-106">Das New-AzMigrateDiskMapping-Cmdlet erstellt eine Zuordnung des Quelldatenträgers, der an den Server angefügt ist, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="e8a6e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8a6e-107">EXAMPLES</span></span>

### <span data-ttu-id="e8a6e-108">Beispiel 1: Erstellen von Datenträgern</span><span class="sxs-lookup"><span data-stu-id="e8a6e-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="e8a6e-109">Datenträgerobjekt zum Bereitstellen von Eingaben für New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="e8a6e-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="e8a6e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8a6e-110">PARAMETERS</span></span>

### <span data-ttu-id="e8a6e-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="e8a6e-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="e8a6e-112">Gibt den datenträgerencyption-Satz an, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="e8a6e-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="e8a6e-113">-DiskID</span></span>
<span data-ttu-id="e8a6e-114">Gibt die Datenträger-ID des Datenträgers an, der an den ermittelten Server angefügt ist, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="e8a6e-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="e8a6e-115">-DiskType</span></span>
<span data-ttu-id="e8a6e-116">Gibt den Typ der Datenträger an, die für die Azure VM verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="e8a6e-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="e8a6e-117">-IsOSDisk</span></span>
<span data-ttu-id="e8a6e-118">Gibt an, ob der Datenträger das Betriebssystem für den Quellserver enthält, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="e8a6e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a6e-119">CommonParameters</span></span>
<span data-ttu-id="e8a6e-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a6e-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8a6e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a6e-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8a6e-122">INPUTS</span></span>

## <span data-ttu-id="e8a6e-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8a6e-123">OUTPUTS</span></span>

### <span data-ttu-id="e8a6e-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="e8a6e-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="e8a6e-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8a6e-125">NOTES</span></span>

<span data-ttu-id="e8a6e-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e8a6e-126">ALIASES</span></span>

## <span data-ttu-id="e8a6e-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8a6e-127">RELATED LINKS</span></span>

