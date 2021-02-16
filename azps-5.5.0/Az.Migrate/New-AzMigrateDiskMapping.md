---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170322"
---
# <span data-ttu-id="fbbcd-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="fbbcd-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="fbbcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbcd-103">Erstellt eine neue Datenträgerzuordnung</span><span class="sxs-lookup"><span data-stu-id="fbbcd-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="fbbcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbbcd-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="fbbcd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbbcd-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbcd-106">Das New-AzMigrateDiskMapping erstellt eine Zuordnung des Quelldatenträgers, der dem Server angefügt ist, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbbcd-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="fbbcd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbbcd-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbcd-108">Beispiel 1: Erstellen von Datenträgern</span><span class="sxs-lookup"><span data-stu-id="fbbcd-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="fbbcd-109">Get disks object to provide input for New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="fbbcd-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="fbbcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbbcd-110">PARAMETERS</span></span>

### <span data-ttu-id="fbbcd-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="fbbcd-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="fbbcd-112">Gibt den zu verwendenden Datenträgerentitätssatz an.</span><span class="sxs-lookup"><span data-stu-id="fbbcd-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="fbbcd-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="fbbcd-113">-DiskID</span></span>
<span data-ttu-id="fbbcd-114">Gibt die Datenträger-ID des Datenträgers an, der an den ermittelten Server angefügt ist, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbbcd-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="fbbcd-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="fbbcd-115">-DiskType</span></span>
<span data-ttu-id="fbbcd-116">Gibt den Datenträgertyp an, der für die Azure VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbbcd-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="fbbcd-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="fbbcd-117">-IsOSDisk</span></span>
<span data-ttu-id="fbbcd-118">Gibt an, ob der Datenträger das Betriebssystem für den zu migrierenden Quellserver enthält.</span><span class="sxs-lookup"><span data-stu-id="fbbcd-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="fbbcd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbcd-119">CommonParameters</span></span>
<span data-ttu-id="fbbcd-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbcd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbcd-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbbcd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbcd-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbcd-122">INPUTS</span></span>

## <span data-ttu-id="fbbcd-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbcd-123">OUTPUTS</span></span>

### <span data-ttu-id="fbbcd-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="fbbcd-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="fbbcd-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbbcd-125">NOTES</span></span>

<span data-ttu-id="fbbcd-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fbbcd-126">ALIASES</span></span>

## <span data-ttu-id="fbbcd-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbbcd-127">RELATED LINKS</span></span>

