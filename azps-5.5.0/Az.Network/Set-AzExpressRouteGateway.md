---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172452"
---
# <span data-ttu-id="8988c-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8988c-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="8988c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8988c-102">SYNOPSIS</span></span>
<span data-ttu-id="8988c-103">Aktualisiert ein skalierbares ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="8988c-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="8988c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8988c-104">SYNTAX</span></span>

### <span data-ttu-id="8988c-105">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8988c-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8988c-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8988c-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8988c-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8988c-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8988c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8988c-108">DESCRIPTION</span></span>

<span data-ttu-id="8988c-109">Mit **dem Cmdlet Set-AzExpressRouteGateway** können Sie die Skalierungseinheiten für ein vorhandenes ExpressRouteGateway oder die Ressourcentags aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8988c-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="8988c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8988c-110">EXAMPLES</span></span>

### <span data-ttu-id="8988c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8988c-111">Example 1</span></span>

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

<span data-ttu-id="8988c-112">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk und ein virtueller Hub in der West-US-Region in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="8988c-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8988c-113">Anschließend wird im virtuellen Hub ein ExpressRoute-Gateway mit 2 Skalierungseinheiten erstellt, das dann in drei Skalierungseinheiten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8988c-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="8988c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8988c-114">PARAMETERS</span></span>

### <span data-ttu-id="8988c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8988c-115">-AsJob</span></span>
<span data-ttu-id="8988c-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8988c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8988c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8988c-117">-DefaultProfile</span></span>
<span data-ttu-id="8988c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8988c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8988c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8988c-119">-InputObject</span></span>
<span data-ttu-id="8988c-120">ExpressRouteGateway, das aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8988c-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="8988c-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="8988c-121">-MaxScaleUnits</span></span>
<span data-ttu-id="8988c-122">Die maximale Anzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="8988c-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="8988c-123">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="8988c-123">Valid range > 2</span></span>

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

### <span data-ttu-id="8988c-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="8988c-124">-MinScaleUnits</span></span>
<span data-ttu-id="8988c-125">Die Mindestanzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="8988c-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="8988c-126">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="8988c-126">Valid range > 2</span></span>

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

### <span data-ttu-id="8988c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8988c-127">-Name</span></span>
<span data-ttu-id="8988c-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8988c-128">The resource name.</span></span>

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

### <span data-ttu-id="8988c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8988c-129">-ResourceGroupName</span></span>
<span data-ttu-id="8988c-130">Der Ressourcengruppenname des expressRouteGateway, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8988c-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="8988c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8988c-131">-ResourceId</span></span>
<span data-ttu-id="8988c-132">Die ID des ExpressRouteGateways, das aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8988c-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="8988c-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="8988c-133">-Tag</span></span>
<span data-ttu-id="8988c-134">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="8988c-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8988c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8988c-135">-Confirm</span></span>
<span data-ttu-id="8988c-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8988c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8988c-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8988c-137">-WhatIf</span></span>
<span data-ttu-id="8988c-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8988c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8988c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8988c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8988c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8988c-140">CommonParameters</span></span>
<span data-ttu-id="8988c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8988c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8988c-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8988c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8988c-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8988c-143">INPUTS</span></span>

### <span data-ttu-id="8988c-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8988c-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="8988c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8988c-145">System.String</span></span>

## <span data-ttu-id="8988c-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8988c-146">OUTPUTS</span></span>

### <span data-ttu-id="8988c-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8988c-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="8988c-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8988c-148">NOTES</span></span>

## <span data-ttu-id="8988c-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8988c-149">RELATED LINKS</span></span>
