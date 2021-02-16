---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155476"
---
# <span data-ttu-id="f897c-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f897c-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f897c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f897c-102">SYNOPSIS</span></span>
<span data-ttu-id="f897c-103">Erstellt eine Nachrichtenanreicherung für ausgewählte Endpunkte in Ihrem IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f897c-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="f897c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f897c-104">SYNTAX</span></span>

### <span data-ttu-id="f897c-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f897c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f897c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f897c-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f897c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f897c-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f897c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f897c-108">DESCRIPTION</span></span>
<span data-ttu-id="f897c-109">Fügen Sie pro IoT Hub bis zu 10 Nachrichtenanreicherungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f897c-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="f897c-110">Diese werden als Anwendungseigenschaften zu Nachrichten hinzugefügt, die an ausgewählte Endpunkte gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f897c-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="f897c-111">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f897c-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f897c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f897c-112">EXAMPLES</span></span>

### <span data-ttu-id="f897c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f897c-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="f897c-114">Fügen Sie eine neue Anreicherung mit dem Schlüssel "newKey" und dem Wert "newValue" hinzu.</span><span class="sxs-lookup"><span data-stu-id="f897c-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="f897c-115">Diese neue Anreicherung wird auf endpunkt1- und "endpunkt2"-Endpunkte angewendet.</span><span class="sxs-lookup"><span data-stu-id="f897c-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="f897c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f897c-116">PARAMETERS</span></span>

### <span data-ttu-id="f897c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f897c-117">-DefaultProfile</span></span>
<span data-ttu-id="f897c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f897c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f897c-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="f897c-119">-Endpoint</span></span>
<span data-ttu-id="f897c-120">Endpunkte, auf die Anreicherungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f897c-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="f897c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f897c-121">-InputObject</span></span>
<span data-ttu-id="f897c-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="f897c-122">IotHub object</span></span>

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

### <span data-ttu-id="f897c-123">-Key</span><span class="sxs-lookup"><span data-stu-id="f897c-123">-Key</span></span>
<span data-ttu-id="f897c-124">Schlüssel der Anreicherung</span><span class="sxs-lookup"><span data-stu-id="f897c-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="f897c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f897c-125">-Name</span></span>
<span data-ttu-id="f897c-126">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="f897c-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f897c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f897c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f897c-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f897c-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f897c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f897c-129">-ResourceId</span></span>
<span data-ttu-id="f897c-130">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f897c-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f897c-131">-Value</span><span class="sxs-lookup"><span data-stu-id="f897c-131">-Value</span></span>
<span data-ttu-id="f897c-132">Der Wert der Anreicherung.</span><span class="sxs-lookup"><span data-stu-id="f897c-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="f897c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f897c-133">-Confirm</span></span>
<span data-ttu-id="f897c-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f897c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f897c-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f897c-135">-WhatIf</span></span>
<span data-ttu-id="f897c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f897c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f897c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f897c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f897c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f897c-138">CommonParameters</span></span>
<span data-ttu-id="f897c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f897c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f897c-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f897c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f897c-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f897c-141">INPUTS</span></span>

### <span data-ttu-id="f897c-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f897c-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f897c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f897c-143">System.String</span></span>

## <span data-ttu-id="f897c-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f897c-144">OUTPUTS</span></span>

### <span data-ttu-id="f897c-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f897c-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="f897c-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f897c-146">NOTES</span></span>

## <span data-ttu-id="f897c-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f897c-147">RELATED LINKS</span></span>
