---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385774"
---
# <span data-ttu-id="fec5e-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="fec5e-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="fec5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec5e-102">SYNOPSIS</span></span>
<span data-ttu-id="fec5e-103">Erstellt ein Objekt zum Aktualisieren der NIC-Eigenschaften eines replizierbaren Servers.</span><span class="sxs-lookup"><span data-stu-id="fec5e-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="fec5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fec5e-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="fec5e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fec5e-105">DESCRIPTION</span></span>
<span data-ttu-id="fec5e-106">Das New-AzMigrateNicMapping erstellt eine Zuordnung der Quell-NIC, die an den Server angefügt ist, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fec5e-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="fec5e-107">Dieses Objekt wird als Eingabe für das cmdlet Set-AzMigrateServerReplication bereitgestellt, um die NIC und ihre Eigenschaften für einen replizierbaren Server zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fec5e-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="fec5e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fec5e-108">EXAMPLES</span></span>

### <span data-ttu-id="fec5e-109">Beispiel 1: Erstellen eines NIC-Objekts</span><span class="sxs-lookup"><span data-stu-id="fec5e-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="fec5e-110">Erstellt ein Aktualisierungsobjekt für NIC.</span><span class="sxs-lookup"><span data-stu-id="fec5e-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="fec5e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec5e-111">PARAMETERS</span></span>

### <span data-ttu-id="fec5e-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="fec5e-112">-NicID</span></span>
<span data-ttu-id="fec5e-113">Gibt die ID der zu aktualisierenden NIC an.</span><span class="sxs-lookup"><span data-stu-id="fec5e-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="fec5e-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="fec5e-114">-TargetNicIP</span></span>
<span data-ttu-id="fec5e-115">Gibt die IP innerhalb des Zielsubnetzs an, das für die NIC verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fec5e-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="fec5e-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="fec5e-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="fec5e-117">Gibt an, ob die zu aktualisierende NIC die primäre, sekundäre oder nicht migrierte NIC ist.</span><span class="sxs-lookup"><span data-stu-id="fec5e-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="fec5e-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="fec5e-118">-TargetNicSubnet</span></span>
<span data-ttu-id="fec5e-119">Gibt den Subnetznamen für die NIC im virtuellen Zielnetzwerk an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="fec5e-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="fec5e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec5e-120">CommonParameters</span></span>
<span data-ttu-id="fec5e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec5e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec5e-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fec5e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec5e-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fec5e-123">INPUTS</span></span>

## <span data-ttu-id="fec5e-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fec5e-124">OUTPUTS</span></span>

### <span data-ttu-id="fec5e-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="fec5e-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="fec5e-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fec5e-126">NOTES</span></span>

<span data-ttu-id="fec5e-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fec5e-127">ALIASES</span></span>

## <span data-ttu-id="fec5e-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fec5e-128">RELATED LINKS</span></span>

