---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179286"
---
# <span data-ttu-id="86083-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="86083-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="86083-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86083-102">SYNOPSIS</span></span>
<span data-ttu-id="86083-103">Abrufen oder Auflisten von Ressourcen für die Näherungs Platzierungs Gruppe</span><span class="sxs-lookup"><span data-stu-id="86083-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="86083-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86083-104">SYNTAX</span></span>

### <span data-ttu-id="86083-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="86083-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86083-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="86083-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86083-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86083-107">DESCRIPTION</span></span>
<span data-ttu-id="86083-108">Dieses Cmdlet ruft die Ressourcen für die Näherungs Platzierungs Gruppe ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="86083-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="86083-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86083-109">EXAMPLES</span></span>

### <span data-ttu-id="86083-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86083-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="86083-111">Dieser Befehl ruft die Gruppe "Näherungs Platzierung" ab.</span><span class="sxs-lookup"><span data-stu-id="86083-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="86083-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="86083-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="86083-113">Dieser Befehl listet alle Proximity-Placement-Gruppen unter der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="86083-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="86083-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="86083-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="86083-115">Dieser Befehl listet alle Proximity-Placement-Gruppen unter dem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="86083-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="86083-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="86083-116">PARAMETERS</span></span>

### <span data-ttu-id="86083-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="86083-117">-ColocationStatus</span></span>
<span data-ttu-id="86083-118">Zeigt den Standortstatus einer Ressource in der Gruppe "Näherungs Platzierung" an.</span><span class="sxs-lookup"><span data-stu-id="86083-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86083-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86083-119">-DefaultProfile</span></span>
<span data-ttu-id="86083-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86083-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86083-121">-Name</span><span class="sxs-lookup"><span data-stu-id="86083-121">-Name</span></span>
<span data-ttu-id="86083-122">Der Name der Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="86083-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="86083-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86083-123">-ResourceGroupName</span></span>
<span data-ttu-id="86083-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="86083-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="86083-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="86083-125">-ResourceId</span></span>
<span data-ttu-id="86083-126">Die Ressourcen-ID für die Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="86083-126">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86083-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86083-127">CommonParameters</span></span>
<span data-ttu-id="86083-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86083-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86083-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86083-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86083-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86083-130">INPUTS</span></span>

### <span data-ttu-id="86083-131">System. String</span><span class="sxs-lookup"><span data-stu-id="86083-131">System.String</span></span>

## <span data-ttu-id="86083-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86083-132">OUTPUTS</span></span>

### <span data-ttu-id="86083-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="86083-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="86083-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="86083-134">NOTES</span></span>

## <span data-ttu-id="86083-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86083-135">RELATED LINKS</span></span>
