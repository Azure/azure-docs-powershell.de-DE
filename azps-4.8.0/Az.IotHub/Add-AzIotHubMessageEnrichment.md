---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175130"
---
# <span data-ttu-id="dad8b-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dad8b-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="dad8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dad8b-102">SYNOPSIS</span></span>
<span data-ttu-id="dad8b-103">Erstellt eine Nachrichten Anreicherung für ausgewählte Endpunkte in Ihrem viel-Hub.</span><span class="sxs-lookup"><span data-stu-id="dad8b-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="dad8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad8b-104">SYNTAX</span></span>

### <span data-ttu-id="dad8b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dad8b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad8b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dad8b-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad8b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dad8b-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad8b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dad8b-108">DESCRIPTION</span></span>
<span data-ttu-id="dad8b-109">Sie können bis zu 10 Nachrichten-Bereicherung pro viel Hub hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dad8b-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="dad8b-110">Diese werden als Anwendungseigenschaften zu Nachrichten hinzugefügt, die an ausgewählte Endpunkte (n) gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="dad8b-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="dad8b-111">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="dad8b-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="dad8b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dad8b-112">EXAMPLES</span></span>

### <span data-ttu-id="dad8b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dad8b-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="dad8b-114">Fügen Sie eine neue Bereicherung mit dem Schlüssel "newkey" und dem Wert "neuer Wert" hinzu.</span><span class="sxs-lookup"><span data-stu-id="dad8b-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="dad8b-115">Diese neue Bereicherung wird auf die Endpunkte "endpoint1" und "endpoint2" angewendet.</span><span class="sxs-lookup"><span data-stu-id="dad8b-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="dad8b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dad8b-116">PARAMETERS</span></span>

### <span data-ttu-id="dad8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad8b-117">-DefaultProfile</span></span>
<span data-ttu-id="dad8b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dad8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad8b-119">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="dad8b-119">-Endpoint</span></span>
<span data-ttu-id="dad8b-120">Endpunkt (e) zum Anwenden von Anreicherung auf.</span><span class="sxs-lookup"><span data-stu-id="dad8b-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dad8b-121">-InputObject</span></span>
<span data-ttu-id="dad8b-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="dad8b-122">IotHub object</span></span>

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

### <span data-ttu-id="dad8b-123">-Taste</span><span class="sxs-lookup"><span data-stu-id="dad8b-123">-Key</span></span>
<span data-ttu-id="dad8b-124">Der Schlüssel der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="dad8b-124">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dad8b-125">-Name</span></span>
<span data-ttu-id="dad8b-126">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="dad8b-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dad8b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad8b-127">-ResourceGroupName</span></span>
<span data-ttu-id="dad8b-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="dad8b-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dad8b-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dad8b-129">-ResourceId</span></span>
<span data-ttu-id="dad8b-130">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dad8b-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dad8b-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="dad8b-131">-Value</span></span>
<span data-ttu-id="dad8b-132">Der Wert der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="dad8b-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="dad8b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dad8b-133">-Confirm</span></span>
<span data-ttu-id="dad8b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dad8b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad8b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad8b-135">-WhatIf</span></span>
<span data-ttu-id="dad8b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dad8b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad8b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dad8b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad8b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad8b-138">CommonParameters</span></span>
<span data-ttu-id="dad8b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad8b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad8b-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad8b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad8b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dad8b-141">INPUTS</span></span>

### <span data-ttu-id="dad8b-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dad8b-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dad8b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dad8b-143">System.String</span></span>

## <span data-ttu-id="dad8b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dad8b-144">OUTPUTS</span></span>

### <span data-ttu-id="dad8b-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dad8b-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="dad8b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="dad8b-146">NOTES</span></span>

## <span data-ttu-id="dad8b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dad8b-147">RELATED LINKS</span></span>
