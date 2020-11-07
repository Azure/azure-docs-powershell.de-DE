---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 5c30db1845fe135aad9ebb575a6b31f19e9598b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842200"
---
# <span data-ttu-id="2d666-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d666-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="2d666-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d666-102">SYNOPSIS</span></span>
<span data-ttu-id="2d666-103">Löschen Sie eine Nachrichten-Bereicherung in Ihrem viel-Hub.</span><span class="sxs-lookup"><span data-stu-id="2d666-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="2d666-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d666-104">SYNTAX</span></span>

### <span data-ttu-id="2d666-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d666-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d666-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2d666-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d666-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2d666-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d666-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d666-108">DESCRIPTION</span></span>
<span data-ttu-id="2d666-109">Eine ausführliche Erläuterung der Nachrichten Anreicherung in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="2d666-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="2d666-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d666-110">EXAMPLES</span></span>

### <span data-ttu-id="2d666-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d666-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="2d666-112">Löscht die "newkey"-Nachrichten Anreicherung.</span><span class="sxs-lookup"><span data-stu-id="2d666-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="2d666-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d666-113">PARAMETERS</span></span>

### <span data-ttu-id="2d666-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d666-114">-DefaultProfile</span></span>
<span data-ttu-id="2d666-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d666-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d666-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d666-116">-InputObject</span></span>
<span data-ttu-id="2d666-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2d666-117">IotHub object</span></span>

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

### <span data-ttu-id="2d666-118">-Taste</span><span class="sxs-lookup"><span data-stu-id="2d666-118">-Key</span></span>
<span data-ttu-id="2d666-119">Der Schlüssel der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="2d666-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="2d666-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2d666-120">-Name</span></span>
<span data-ttu-id="2d666-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="2d666-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2d666-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d666-122">-PassThru</span></span>
<span data-ttu-id="2d666-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="2d666-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="2d666-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2d666-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d666-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d666-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d666-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2d666-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2d666-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2d666-127">-ResourceId</span></span>
<span data-ttu-id="2d666-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2d666-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2d666-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d666-129">-Confirm</span></span>
<span data-ttu-id="2d666-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d666-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d666-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d666-131">-WhatIf</span></span>
<span data-ttu-id="2d666-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d666-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d666-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d666-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d666-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d666-134">CommonParameters</span></span>
<span data-ttu-id="2d666-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d666-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d666-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d666-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d666-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d666-137">INPUTS</span></span>

### <span data-ttu-id="2d666-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2d666-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2d666-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2d666-139">System.String</span></span>

## <span data-ttu-id="2d666-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d666-140">OUTPUTS</span></span>

### <span data-ttu-id="2d666-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d666-141">System.Boolean</span></span>

## <span data-ttu-id="2d666-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d666-142">NOTES</span></span>

## <span data-ttu-id="2d666-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d666-143">RELATED LINKS</span></span>
