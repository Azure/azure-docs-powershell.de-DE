---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174717"
---
# <span data-ttu-id="91912-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="91912-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="91912-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91912-102">SYNOPSIS</span></span>
<span data-ttu-id="91912-103">Löschen eines Endpunkts für Ihren viel Hub</span><span class="sxs-lookup"><span data-stu-id="91912-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="91912-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91912-104">SYNTAX</span></span>

### <span data-ttu-id="91912-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91912-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91912-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91912-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91912-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91912-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91912-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91912-108">DESCRIPTION</span></span>
<span data-ttu-id="91912-109">Löschen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="91912-109">Delete an endpoint.</span></span> <span data-ttu-id="91912-110">Vergessen Sie nicht, alle Routen zu löschen, die diesen Endpunkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="91912-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="91912-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91912-111">EXAMPLES</span></span>

### <span data-ttu-id="91912-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91912-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="91912-113">Löschen Sie den Endpunkt "E2" aus "myiothub" viel Hub.</span><span class="sxs-lookup"><span data-stu-id="91912-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="91912-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="91912-114">PARAMETERS</span></span>

### <span data-ttu-id="91912-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91912-115">-DefaultProfile</span></span>
<span data-ttu-id="91912-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91912-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91912-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="91912-117">-EndpointName</span></span>
<span data-ttu-id="91912-118">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="91912-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="91912-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="91912-119">-EndpointType</span></span>
<span data-ttu-id="91912-120">Typ des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="91912-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91912-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91912-121">-InputObject</span></span>
<span data-ttu-id="91912-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="91912-122">IotHub Object</span></span>

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

### <span data-ttu-id="91912-123">-Name</span><span class="sxs-lookup"><span data-stu-id="91912-123">-Name</span></span>
<span data-ttu-id="91912-124">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="91912-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="91912-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91912-125">-PassThru</span></span>
<span data-ttu-id="91912-126">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="91912-126">Allows to return the boolean object.</span></span> <span data-ttu-id="91912-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="91912-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91912-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91912-128">-ResourceGroupName</span></span>
<span data-ttu-id="91912-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="91912-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91912-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="91912-130">-ResourceId</span></span>
<span data-ttu-id="91912-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="91912-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="91912-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91912-132">-Confirm</span></span>
<span data-ttu-id="91912-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91912-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91912-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91912-134">-WhatIf</span></span>
<span data-ttu-id="91912-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91912-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91912-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91912-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91912-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91912-137">CommonParameters</span></span>
<span data-ttu-id="91912-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91912-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91912-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91912-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91912-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91912-140">INPUTS</span></span>

### <span data-ttu-id="91912-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="91912-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="91912-142">System. String</span><span class="sxs-lookup"><span data-stu-id="91912-142">System.String</span></span>

## <span data-ttu-id="91912-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91912-143">OUTPUTS</span></span>

### <span data-ttu-id="91912-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91912-144">System.Boolean</span></span>

## <span data-ttu-id="91912-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="91912-145">NOTES</span></span>

## <span data-ttu-id="91912-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91912-146">RELATED LINKS</span></span>
