---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356795"
---
# <span data-ttu-id="3370f-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="3370f-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="3370f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3370f-102">SYNOPSIS</span></span>
<span data-ttu-id="3370f-103">Erstellt ein Objekt zum Aktualisieren der NIC-Eigenschaften eines replizierbaren Servers.</span><span class="sxs-lookup"><span data-stu-id="3370f-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="3370f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3370f-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="3370f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3370f-105">DESCRIPTION</span></span>
<span data-ttu-id="3370f-106">Das New-AzMigrateNicMapping erstellt eine Zuordnung der Quell-NIC, die an den Server angefügt ist, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3370f-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="3370f-107">Dieses Objekt wird als Eingabe für das cmdlet Set-AzMigrateServerReplication bereitgestellt, um die NIC und ihre Eigenschaften für einen replizierbaren Server zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3370f-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="3370f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3370f-108">EXAMPLES</span></span>

### <span data-ttu-id="3370f-109">Beispiel 1: Erstellen eines NIC-Objekts</span><span class="sxs-lookup"><span data-stu-id="3370f-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="3370f-110">Erstellt ein Aktualisierungsobjekt für NIC.</span><span class="sxs-lookup"><span data-stu-id="3370f-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="3370f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3370f-111">PARAMETERS</span></span>

### <span data-ttu-id="3370f-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="3370f-112">-NicID</span></span>
<span data-ttu-id="3370f-113">Gibt die ID der zu aktualisierenden NIC an.</span><span class="sxs-lookup"><span data-stu-id="3370f-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="3370f-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="3370f-114">-TargetNicIP</span></span>
<span data-ttu-id="3370f-115">Gibt die IP innerhalb des Zielsubnetzs an, das für die NIC verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3370f-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="3370f-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="3370f-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="3370f-117">Gibt an, ob die zu aktualisierende NIC die primäre, sekundäre oder nicht migrierte NIC ist.</span><span class="sxs-lookup"><span data-stu-id="3370f-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="3370f-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="3370f-118">-TargetNicSubnet</span></span>
<span data-ttu-id="3370f-119">Gibt den Subnetznamen für die NIC im virtuellen Zielnetzwerk an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3370f-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="3370f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3370f-120">CommonParameters</span></span>
<span data-ttu-id="3370f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3370f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3370f-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3370f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3370f-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3370f-123">INPUTS</span></span>

## <span data-ttu-id="3370f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3370f-124">OUTPUTS</span></span>

### <span data-ttu-id="3370f-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="3370f-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="3370f-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3370f-126">NOTES</span></span>

<span data-ttu-id="3370f-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3370f-127">ALIASES</span></span>

## <span data-ttu-id="3370f-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3370f-128">RELATED LINKS</span></span>

