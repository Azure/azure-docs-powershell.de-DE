---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166451"
---
# <span data-ttu-id="422bd-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="422bd-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="422bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="422bd-102">SYNOPSIS</span></span>
<span data-ttu-id="422bd-103">Löschen Sie eine Nachrichten-Bereicherung in Ihrem viel-Hub.</span><span class="sxs-lookup"><span data-stu-id="422bd-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="422bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="422bd-104">SYNTAX</span></span>

### <span data-ttu-id="422bd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="422bd-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="422bd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="422bd-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="422bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="422bd-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="422bd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="422bd-108">DESCRIPTION</span></span>
<span data-ttu-id="422bd-109">Eine ausführliche Erläuterung der Nachrichten Anreicherung in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="422bd-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="422bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="422bd-110">EXAMPLES</span></span>

### <span data-ttu-id="422bd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="422bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="422bd-112">Löscht die "newkey"-Nachrichten Anreicherung.</span><span class="sxs-lookup"><span data-stu-id="422bd-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="422bd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="422bd-113">PARAMETERS</span></span>

### <span data-ttu-id="422bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422bd-114">-DefaultProfile</span></span>
<span data-ttu-id="422bd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="422bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="422bd-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="422bd-116">-InputObject</span></span>
<span data-ttu-id="422bd-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="422bd-117">IotHub object</span></span>

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

### <span data-ttu-id="422bd-118">-Taste</span><span class="sxs-lookup"><span data-stu-id="422bd-118">-Key</span></span>
<span data-ttu-id="422bd-119">Der Schlüssel der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="422bd-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="422bd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="422bd-120">-Name</span></span>
<span data-ttu-id="422bd-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="422bd-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="422bd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="422bd-122">-PassThru</span></span>
<span data-ttu-id="422bd-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="422bd-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="422bd-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="422bd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="422bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="422bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="422bd-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="422bd-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="422bd-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="422bd-127">-ResourceId</span></span>
<span data-ttu-id="422bd-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="422bd-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="422bd-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="422bd-129">-Confirm</span></span>
<span data-ttu-id="422bd-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="422bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="422bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="422bd-131">-WhatIf</span></span>
<span data-ttu-id="422bd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="422bd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="422bd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="422bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="422bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422bd-134">CommonParameters</span></span>
<span data-ttu-id="422bd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="422bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422bd-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="422bd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422bd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="422bd-137">INPUTS</span></span>

### <span data-ttu-id="422bd-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="422bd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="422bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="422bd-139">System.String</span></span>

## <span data-ttu-id="422bd-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="422bd-140">OUTPUTS</span></span>

### <span data-ttu-id="422bd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="422bd-141">System.Boolean</span></span>

## <span data-ttu-id="422bd-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="422bd-142">NOTES</span></span>

## <span data-ttu-id="422bd-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="422bd-143">RELATED LINKS</span></span>
