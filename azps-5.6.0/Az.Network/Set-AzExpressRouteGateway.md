---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: faa634facf6baa8d0d55490ec32a9395feaea5db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924608"
---
# <span data-ttu-id="74c69-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="74c69-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="74c69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c69-102">SYNOPSIS</span></span>
<span data-ttu-id="74c69-103">Aktualisiert ein skalierbares ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="74c69-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="74c69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74c69-104">SYNTAX</span></span>

### <span data-ttu-id="74c69-105">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="74c69-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74c69-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="74c69-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74c69-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="74c69-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74c69-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74c69-108">DESCRIPTION</span></span>

<span data-ttu-id="74c69-109">Mit **dem Set-AzExpressRouteGateway-Cmdlet** können Sie die Skalierungseinheiten für ein vorhandenes ExpressRouteGateway aktualisieren oder die Ressourcentags aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="74c69-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="74c69-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74c69-110">EXAMPLES</span></span>

### <span data-ttu-id="74c69-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74c69-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="74c69-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="74c69-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="74c69-113">Anschließend wird im virtuellen Hub ein ExpressRoute-Gateway mit zwei Skalierungseinheiten erstellt, das dann in 3 Skalierungseinheiten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="74c69-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="74c69-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="74c69-114">PARAMETERS</span></span>

### <span data-ttu-id="74c69-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74c69-115">-AsJob</span></span>
<span data-ttu-id="74c69-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74c69-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c69-117">-DefaultProfile</span></span>
<span data-ttu-id="74c69-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74c69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c69-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74c69-119">-InputObject</span></span>
<span data-ttu-id="74c69-120">Das ExpressRouteGateway, das aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="74c69-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="74c69-121">-MaxScaleUnits</span></span>
<span data-ttu-id="74c69-122">Die maximale Anzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="74c69-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="74c69-123">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="74c69-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="74c69-124">-MinScaleUnits</span></span>
<span data-ttu-id="74c69-125">Die Mindestanzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="74c69-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="74c69-126">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="74c69-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-127">-Name</span><span class="sxs-lookup"><span data-stu-id="74c69-127">-Name</span></span>
<span data-ttu-id="74c69-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="74c69-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c69-129">-ResourceGroupName</span></span>
<span data-ttu-id="74c69-130">Der Ressourcengruppenname des ExpressRouteGateways, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="74c69-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74c69-131">-ResourceId</span></span>
<span data-ttu-id="74c69-132">Die ID des ExpressRouteGateways, das aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="74c69-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="74c69-133">-Tag</span></span>
<span data-ttu-id="74c69-134">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="74c69-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74c69-135">-Confirm</span></span>
<span data-ttu-id="74c69-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74c69-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c69-137">-WhatIf</span></span>
<span data-ttu-id="74c69-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74c69-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c69-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74c69-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c69-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c69-140">CommonParameters</span></span>
<span data-ttu-id="74c69-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c69-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c69-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c69-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c69-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74c69-143">INPUTS</span></span>

### <span data-ttu-id="74c69-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="74c69-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="74c69-145">System.String</span><span class="sxs-lookup"><span data-stu-id="74c69-145">System.String</span></span>

## <span data-ttu-id="74c69-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74c69-146">OUTPUTS</span></span>

### <span data-ttu-id="74c69-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="74c69-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="74c69-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="74c69-148">NOTES</span></span>

## <span data-ttu-id="74c69-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="74c69-149">RELATED LINKS</span></span>
