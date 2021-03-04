---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 7a69b47cef0d1f2ad11dcbe1c2bd191149d127df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949592"
---
# <span data-ttu-id="6914a-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6914a-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="6914a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6914a-102">SYNOPSIS</span></span>
<span data-ttu-id="6914a-103">Ressourcen der Näherungsplatzierungsgruppe(en) erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="6914a-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="6914a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6914a-104">SYNTAX</span></span>

### <span data-ttu-id="6914a-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="6914a-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6914a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6914a-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6914a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6914a-107">DESCRIPTION</span></span>
<span data-ttu-id="6914a-108">Dieses Cmdlet wird Ressourcen der Näherungsplatzierungsgruppe(en) erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="6914a-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="6914a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6914a-109">EXAMPLES</span></span>

### <span data-ttu-id="6914a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6914a-110">Example 1</span></span>
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

<span data-ttu-id="6914a-111">Dieser Befehl ruft die Näherungsplatzierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6914a-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="6914a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6914a-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="6914a-113">Dieser Befehl listet alle Näherungsplatzierungsgruppen unter der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="6914a-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="6914a-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6914a-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="6914a-115">Dieser Befehl listet alle Näherungsplatzierungsgruppen unter dem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="6914a-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="6914a-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6914a-116">PARAMETERS</span></span>

### <span data-ttu-id="6914a-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="6914a-117">-ColocationStatus</span></span>
<span data-ttu-id="6914a-118">Zeigt den Colocation-Status einer Ressource in der Näherungsplatzierungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="6914a-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="6914a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6914a-119">-DefaultProfile</span></span>
<span data-ttu-id="6914a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6914a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6914a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6914a-121">-Name</span></span>
<span data-ttu-id="6914a-122">Der Name der Näherungsplatzierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6914a-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="6914a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6914a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6914a-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6914a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6914a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6914a-125">-ResourceId</span></span>
<span data-ttu-id="6914a-126">Die Ressourcen-ID für die Näherungsplatzierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6914a-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="6914a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6914a-127">CommonParameters</span></span>
<span data-ttu-id="6914a-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6914a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6914a-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6914a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6914a-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6914a-130">INPUTS</span></span>

### <span data-ttu-id="6914a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6914a-131">System.String</span></span>

## <span data-ttu-id="6914a-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6914a-132">OUTPUTS</span></span>

### <span data-ttu-id="6914a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6914a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="6914a-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6914a-134">NOTES</span></span>

## <span data-ttu-id="6914a-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6914a-135">RELATED LINKS</span></span>
