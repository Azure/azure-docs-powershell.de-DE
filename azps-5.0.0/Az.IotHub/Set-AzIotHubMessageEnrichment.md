---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180453"
---
# <span data-ttu-id="5d45c-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d45c-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="5d45c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d45c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d45c-103">Aktualisieren Sie eine Nachrichten Anreicherung in Ihrem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="5d45c-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="5d45c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d45c-104">SYNTAX</span></span>

### <span data-ttu-id="5d45c-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d45c-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d45c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d45c-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d45c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5d45c-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d45c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d45c-108">DESCRIPTION</span></span>
<span data-ttu-id="5d45c-109">Eine ausführliche Erläuterung der Nachrichten Anreicherung in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="5d45c-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="5d45c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d45c-110">EXAMPLES</span></span>

### <span data-ttu-id="5d45c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d45c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="5d45c-112">Aktualisiert den Wert der Bereicherung auf "UpdatedValue" für den Schlüssel "newkey".</span><span class="sxs-lookup"><span data-stu-id="5d45c-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="5d45c-113">Eine ausführliche Erläuterung der Nachrichten Anreicherung in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="5d45c-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="5d45c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d45c-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="5d45c-115">Aktualisiert den Endpunkt der Bereicherung auf "endpoint1, endpoint2, endpoint3" für den Schlüssel "newkey".</span><span class="sxs-lookup"><span data-stu-id="5d45c-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="5d45c-116">Eine ausführliche Erläuterung der Nachrichten Anreicherung in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="5d45c-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="5d45c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d45c-117">PARAMETERS</span></span>

### <span data-ttu-id="5d45c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d45c-118">-DefaultProfile</span></span>
<span data-ttu-id="5d45c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d45c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d45c-120">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5d45c-120">-Endpoint</span></span>
<span data-ttu-id="5d45c-121">Endpunkt (e) zum Anwenden von Anreicherung auf.</span><span class="sxs-lookup"><span data-stu-id="5d45c-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d45c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d45c-122">-InputObject</span></span>
<span data-ttu-id="5d45c-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="5d45c-123">IotHub Object</span></span>

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

### <span data-ttu-id="5d45c-124">-Taste</span><span class="sxs-lookup"><span data-stu-id="5d45c-124">-Key</span></span>
<span data-ttu-id="5d45c-125">Der Schlüssel der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="5d45c-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="5d45c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5d45c-126">-Name</span></span>
<span data-ttu-id="5d45c-127">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="5d45c-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5d45c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d45c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d45c-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5d45c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5d45c-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5d45c-130">-ResourceId</span></span>
<span data-ttu-id="5d45c-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5d45c-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5d45c-132">-Wert</span><span class="sxs-lookup"><span data-stu-id="5d45c-132">-Value</span></span>
<span data-ttu-id="5d45c-133">Der Wert der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="5d45c-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="5d45c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d45c-134">-Confirm</span></span>
<span data-ttu-id="5d45c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d45c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d45c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d45c-136">-WhatIf</span></span>
<span data-ttu-id="5d45c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d45c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d45c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d45c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d45c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d45c-139">CommonParameters</span></span>
<span data-ttu-id="5d45c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d45c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d45c-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d45c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d45c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d45c-142">INPUTS</span></span>

### <span data-ttu-id="5d45c-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5d45c-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5d45c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5d45c-144">System.String</span></span>

## <span data-ttu-id="5d45c-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d45c-145">OUTPUTS</span></span>

### <span data-ttu-id="5d45c-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="5d45c-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="5d45c-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d45c-147">NOTES</span></span>

## <span data-ttu-id="5d45c-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d45c-148">RELATED LINKS</span></span>
