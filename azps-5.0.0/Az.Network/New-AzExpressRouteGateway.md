---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179868"
---
# <span data-ttu-id="59f54-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="59f54-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="59f54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59f54-102">SYNOPSIS</span></span>
<span data-ttu-id="59f54-103">Erstellt ein skalierbares Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="59f54-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="59f54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59f54-104">SYNTAX</span></span>

### <span data-ttu-id="59f54-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="59f54-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f54-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="59f54-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f54-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="59f54-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f54-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59f54-108">DESCRIPTION</span></span>

<span data-ttu-id="59f54-109">New-AzExpressRouteGateway erstellt ein skalierbares Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="59f54-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="59f54-110">Hierbei handelt es sich um Software definierte Konnektivität für On Premise to Azure innerhalb des VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="59f54-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="59f54-111">Dieses Gateway kann basierend auf der in diesem oder dem Set-AzExpressRouteGateway-Cmdlet angegebenen Skalierungseinheit skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="59f54-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="59f54-112">Eine Verbindung wird von einem lokalen Express Route-Schaltkreis mit dem skalierbaren Gateway eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="59f54-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="59f54-113">Die ExpressRouteGateway befindet sich am gleichen Speicherort wie die referenzierte VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="59f54-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="59f54-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59f54-114">EXAMPLES</span></span>

### <span data-ttu-id="59f54-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59f54-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="59f54-116">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="59f54-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="59f54-117">Anschließend wird ein Express Route-Gateway im virtuellen Hub mit zwei Skaleneinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="59f54-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="59f54-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="59f54-118">PARAMETERS</span></span>

### <span data-ttu-id="59f54-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59f54-119">-AsJob</span></span>
<span data-ttu-id="59f54-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="59f54-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59f54-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f54-121">-DefaultProfile</span></span>
<span data-ttu-id="59f54-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59f54-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f54-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="59f54-123">-MaxScaleUnits</span></span>
<span data-ttu-id="59f54-124">Die maximale Anzahl von Skalierungseinheiten für diesen ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="59f54-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="59f54-125">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="59f54-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f54-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="59f54-126">-MinScaleUnits</span></span>
<span data-ttu-id="59f54-127">Die minimale Anzahl von Skalierungseinheiten für diesen ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="59f54-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="59f54-128">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="59f54-128">Valid range > 2</span></span>

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

### <span data-ttu-id="59f54-129">-Name</span><span class="sxs-lookup"><span data-stu-id="59f54-129">-Name</span></span>
<span data-ttu-id="59f54-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="59f54-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f54-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f54-131">-ResourceGroupName</span></span>
<span data-ttu-id="59f54-132">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="59f54-132">The resource name.</span></span>

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

### <span data-ttu-id="59f54-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="59f54-133">-Tag</span></span>
<span data-ttu-id="59f54-134">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="59f54-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="59f54-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="59f54-135">-VirtualHub</span></span>
<span data-ttu-id="59f54-136">Das VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="59f54-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59f54-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="59f54-137">-VirtualHubId</span></span>
<span data-ttu-id="59f54-138">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="59f54-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f54-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="59f54-139">-VirtualHubName</span></span>
<span data-ttu-id="59f54-140">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="59f54-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f54-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59f54-141">-Confirm</span></span>
<span data-ttu-id="59f54-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59f54-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f54-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f54-143">-WhatIf</span></span>
<span data-ttu-id="59f54-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59f54-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f54-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59f54-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f54-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f54-146">CommonParameters</span></span>
<span data-ttu-id="59f54-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f54-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f54-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f54-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f54-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59f54-149">INPUTS</span></span>

### <span data-ttu-id="59f54-150">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="59f54-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="59f54-151">System. String</span><span class="sxs-lookup"><span data-stu-id="59f54-151">System.String</span></span>

## <span data-ttu-id="59f54-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59f54-152">OUTPUTS</span></span>

### <span data-ttu-id="59f54-153">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="59f54-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="59f54-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="59f54-154">NOTES</span></span>

## <span data-ttu-id="59f54-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59f54-155">RELATED LINKS</span></span>
