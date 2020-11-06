---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503653"
---
# <span data-ttu-id="76c02-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="76c02-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="76c02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76c02-102">SYNOPSIS</span></span>
<span data-ttu-id="76c02-103">Löschen eines Endpunkts für Ihren viel Hub</span><span class="sxs-lookup"><span data-stu-id="76c02-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76c02-104">SYNTAX</span></span>

### <span data-ttu-id="76c02-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="76c02-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76c02-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76c02-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76c02-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="76c02-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76c02-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76c02-108">DESCRIPTION</span></span>
<span data-ttu-id="76c02-109">Löschen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="76c02-109">Delete an endpoint.</span></span> <span data-ttu-id="76c02-110">Vergessen Sie nicht, alle Routen zu löschen, die diesen Endpunkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="76c02-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="76c02-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76c02-111">EXAMPLES</span></span>

### <span data-ttu-id="76c02-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76c02-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="76c02-113">Löschen Sie den Endpunkt "E2" aus "myiothub" viel Hub.</span><span class="sxs-lookup"><span data-stu-id="76c02-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="76c02-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="76c02-114">PARAMETERS</span></span>

### <span data-ttu-id="76c02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c02-115">-DefaultProfile</span></span>
<span data-ttu-id="76c02-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76c02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c02-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="76c02-117">-EndpointName</span></span>
<span data-ttu-id="76c02-118">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="76c02-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="76c02-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="76c02-119">-EndpointType</span></span>
<span data-ttu-id="76c02-120">Typ des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="76c02-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c02-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76c02-121">-InputObject</span></span>
<span data-ttu-id="76c02-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="76c02-122">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76c02-123">-Name</span><span class="sxs-lookup"><span data-stu-id="76c02-123">-Name</span></span>
<span data-ttu-id="76c02-124">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="76c02-124">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c02-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76c02-125">-PassThru</span></span>
<span data-ttu-id="76c02-126">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="76c02-126">Allows to return the boolean object.</span></span> <span data-ttu-id="76c02-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="76c02-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76c02-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c02-128">-ResourceGroupName</span></span>
<span data-ttu-id="76c02-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="76c02-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c02-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="76c02-130">-ResourceId</span></span>
<span data-ttu-id="76c02-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="76c02-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c02-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76c02-132">-Confirm</span></span>
<span data-ttu-id="76c02-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76c02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c02-134">-WhatIf</span></span>
<span data-ttu-id="76c02-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76c02-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c02-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76c02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c02-137">CommonParameters</span></span>
<span data-ttu-id="76c02-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c02-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c02-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c02-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76c02-140">INPUTS</span></span>

### <span data-ttu-id="76c02-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="76c02-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="76c02-142">System. String</span><span class="sxs-lookup"><span data-stu-id="76c02-142">System.String</span></span>

## <span data-ttu-id="76c02-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76c02-143">OUTPUTS</span></span>

### <span data-ttu-id="76c02-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="76c02-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="76c02-145">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. IotHub. Models. PSRoutingCustomEndpoint, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="76c02-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="76c02-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="76c02-146">NOTES</span></span>

## <span data-ttu-id="76c02-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76c02-147">RELATED LINKS</span></span>
