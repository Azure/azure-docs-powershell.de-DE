---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179076"
---
# <span data-ttu-id="9d124-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="9d124-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="9d124-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d124-102">SYNOPSIS</span></span>
<span data-ttu-id="9d124-103">Erstellt ein Objekt, um die NIC-Eigenschaften eines replizierenden Servers zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9d124-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="9d124-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d124-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d124-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d124-105">DESCRIPTION</span></span>
<span data-ttu-id="9d124-106">Das New-AzMigrateNicMapping-Cmdlet erstellt eine Zuordnung der Quell-NIC, die mit dem zu migrierenden Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9d124-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="9d124-107">Dieses Objekt wird als Eingabe für das Set-AzMigrateServerReplication-Cmdlet bereitgestellt, um die NIC und ihre Eigenschaften für einen replizierenden Server zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9d124-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="9d124-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d124-108">EXAMPLES</span></span>

### <span data-ttu-id="9d124-109">Beispiel 1: Erstellen eines NIC-Objekts</span><span class="sxs-lookup"><span data-stu-id="9d124-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="9d124-110">Erstellt ein NIC-Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d124-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="9d124-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d124-111">PARAMETERS</span></span>

### <span data-ttu-id="9d124-112">-Nicid</span><span class="sxs-lookup"><span data-stu-id="9d124-112">-NicID</span></span>
<span data-ttu-id="9d124-113">Gibt die ID der zu aktualisierende NIC an.</span><span class="sxs-lookup"><span data-stu-id="9d124-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="9d124-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="9d124-114">-TargetNicIP</span></span>
<span data-ttu-id="9d124-115">Gibt die IP-Adresse im Ziel-Subnetz an, die für die NIC verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d124-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="9d124-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="9d124-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="9d124-117">Gibt an, ob die zu Aktualisier endnic die primäre, sekundäre oder nicht migrierte NIC ist.</span><span class="sxs-lookup"><span data-stu-id="9d124-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="9d124-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="9d124-118">-TargetNicSubnet</span></span>
<span data-ttu-id="9d124-119">Gibt den Subnet-Namen für die NIC im virtuellen Zielnetzwerk an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9d124-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="9d124-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d124-120">CommonParameters</span></span>
<span data-ttu-id="9d124-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d124-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d124-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d124-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d124-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d124-123">INPUTS</span></span>

## <span data-ttu-id="9d124-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d124-124">OUTPUTS</span></span>

### <span data-ttu-id="9d124-125">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="9d124-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="9d124-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d124-126">NOTES</span></span>

<span data-ttu-id="9d124-127">Aliase</span><span class="sxs-lookup"><span data-stu-id="9d124-127">ALIASES</span></span>

## <span data-ttu-id="9d124-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d124-128">RELATED LINKS</span></span>

