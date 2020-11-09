---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: 7cc9dbe5c4727c283ead66e88b6c52c9c2fcd00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301408"
---
# <span data-ttu-id="16992-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="16992-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="16992-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16992-102">SYNOPSIS</span></span>
<span data-ttu-id="16992-103">Aktualisiert ein skalierbares Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="16992-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="16992-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16992-104">SYNTAX</span></span>

### <span data-ttu-id="16992-105">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="16992-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16992-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="16992-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16992-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="16992-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16992-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16992-108">DESCRIPTION</span></span>

<span data-ttu-id="16992-109">Set-AzExpressRouteGateway aktualisiert die Skalierungseinheiten für die ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="16992-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="16992-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16992-110">EXAMPLES</span></span>

### <span data-ttu-id="16992-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16992-111">Example 1</span></span>

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

<span data-ttu-id="16992-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="16992-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="16992-113">Anschließend wird ein Express Route-Gateway im virtuellen Hub mit 2 Skaleneinheiten erstellt, die dann auf 3 Skaleneinheiten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="16992-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="16992-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="16992-114">PARAMETERS</span></span>

### <span data-ttu-id="16992-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16992-115">-AsJob</span></span>
<span data-ttu-id="16992-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="16992-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16992-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16992-117">-DefaultProfile</span></span>
<span data-ttu-id="16992-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16992-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16992-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16992-119">-InputObject</span></span>
<span data-ttu-id="16992-120">Die ExpressRouteGateway, die aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="16992-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="16992-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="16992-121">-MaxScaleUnits</span></span>
<span data-ttu-id="16992-122">Die maximale Anzahl von Skalierungseinheiten für diesen ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="16992-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="16992-123">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="16992-123">Valid range > 2</span></span>

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

### <span data-ttu-id="16992-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="16992-124">-MinScaleUnits</span></span>
<span data-ttu-id="16992-125">Die minimale Anzahl von Skalierungseinheiten für diesen ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="16992-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="16992-126">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="16992-126">Valid range > 2</span></span>

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

### <span data-ttu-id="16992-127">-Name</span><span class="sxs-lookup"><span data-stu-id="16992-127">-Name</span></span>
<span data-ttu-id="16992-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="16992-128">The resource name.</span></span>

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

### <span data-ttu-id="16992-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16992-129">-ResourceGroupName</span></span>
<span data-ttu-id="16992-130">Der Ressourcengruppenname des ExpressRouteGateway, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="16992-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="16992-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16992-131">-ResourceId</span></span>
<span data-ttu-id="16992-132">Die ID des ExpressRouteGateway, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="16992-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="16992-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="16992-133">-Tag</span></span>
<span data-ttu-id="16992-134">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="16992-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="16992-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16992-135">-Confirm</span></span>
<span data-ttu-id="16992-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16992-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16992-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16992-137">-WhatIf</span></span>
<span data-ttu-id="16992-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16992-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16992-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16992-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16992-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16992-140">CommonParameters</span></span>
<span data-ttu-id="16992-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16992-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16992-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16992-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16992-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16992-143">INPUTS</span></span>

### <span data-ttu-id="16992-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="16992-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="16992-145">System. String</span><span class="sxs-lookup"><span data-stu-id="16992-145">System.String</span></span>

## <span data-ttu-id="16992-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16992-146">OUTPUTS</span></span>

### <span data-ttu-id="16992-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="16992-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="16992-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="16992-148">NOTES</span></span>

## <span data-ttu-id="16992-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16992-149">RELATED LINKS</span></span>
