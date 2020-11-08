---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: 6e83def7c4956e4936e8e3c55f96aab1da0d451d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996472"
---
# <span data-ttu-id="0a12b-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a12b-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="0a12b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a12b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a12b-103">Erstellt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0a12b-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="0a12b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a12b-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a12b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a12b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a12b-106">Das Cmdlet **New-AzPrivateEndpoint** erstellt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="0a12b-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="0a12b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a12b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a12b-108">1: Erstellen eines privaten Endpunkts</span><span class="sxs-lookup"><span data-stu-id="0a12b-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="0a12b-109">In diesem Beispiel wird ein privater Endpunkt mit bestimmter privater Link Dienst-ID in einem bestimmten Subnetz in einem virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a12b-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="0a12b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a12b-110">PARAMETERS</span></span>

### <span data-ttu-id="0a12b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a12b-111">-AsJob</span></span>
<span data-ttu-id="0a12b-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0a12b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a12b-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="0a12b-113">-ByManualRequest</span></span>
<span data-ttu-id="0a12b-114">Verwenden der manuellen Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a12b-114">Using manual request.</span></span>

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

### <span data-ttu-id="0a12b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a12b-115">-DefaultProfile</span></span>
<span data-ttu-id="0a12b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a12b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a12b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0a12b-117">-Force</span></span>
<span data-ttu-id="0a12b-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="0a12b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0a12b-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="0a12b-119">-Location</span></span>
<span data-ttu-id="0a12b-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="0a12b-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0a12b-121">-Name</span></span>
<span data-ttu-id="0a12b-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0a12b-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0a12b-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="0a12b-124">Die Verbindung des privaten Verbindungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="0a12b-124">The private link service connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a12b-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a12b-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a12b-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-127">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="0a12b-127">-Subnet</span></span>
<span data-ttu-id="0a12b-128">Das Subnetz des privaten Endpunkts</span><span class="sxs-lookup"><span data-stu-id="0a12b-128">The subnet of the private endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a12b-129">-Tag</span></span>
<span data-ttu-id="0a12b-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0a12b-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a12b-131">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0a12b-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a12b-132">-Confirm</span></span>
<span data-ttu-id="0a12b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a12b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a12b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a12b-134">-WhatIf</span></span>
<span data-ttu-id="0a12b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a12b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a12b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a12b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a12b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a12b-137">CommonParameters</span></span>
<span data-ttu-id="0a12b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a12b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a12b-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a12b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a12b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a12b-140">INPUTS</span></span>

### <span data-ttu-id="0a12b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0a12b-141">System.String</span></span>

### <span data-ttu-id="0a12b-142">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0a12b-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="0a12b-143">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="0a12b-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="0a12b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a12b-144">OUTPUTS</span></span>

### <span data-ttu-id="0a12b-145">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a12b-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="0a12b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a12b-146">NOTES</span></span>

## <span data-ttu-id="0a12b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a12b-147">RELATED LINKS</span></span>

[<span data-ttu-id="0a12b-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a12b-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="0a12b-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a12b-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="0a12b-150">Neu – AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0a12b-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)