---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292732"
---
# <span data-ttu-id="8cc64-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8cc64-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="8cc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc64-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc64-103">Löschen Sie eine Nachrichtenanreicherung in Ihrem IoT-Hub.</span><span class="sxs-lookup"><span data-stu-id="8cc64-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="8cc64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cc64-104">SYNTAX</span></span>

### <span data-ttu-id="8cc64-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8cc64-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc64-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cc64-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc64-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8cc64-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc64-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cc64-108">DESCRIPTION</span></span>
<span data-ttu-id="8cc64-109">Eine ausführliche Erläuterung der Nachrichtenanreicherung in Azure IoT Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="8cc64-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="8cc64-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8cc64-110">EXAMPLES</span></span>

### <span data-ttu-id="8cc64-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cc64-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="8cc64-112">Löscht die Nachrichtenanreicherung "newKey".</span><span class="sxs-lookup"><span data-stu-id="8cc64-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="8cc64-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cc64-113">PARAMETERS</span></span>

### <span data-ttu-id="8cc64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc64-114">-DefaultProfile</span></span>
<span data-ttu-id="8cc64-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cc64-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc64-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cc64-116">-InputObject</span></span>
<span data-ttu-id="8cc64-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="8cc64-117">IotHub object</span></span>

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

### <span data-ttu-id="8cc64-118">-Key</span><span class="sxs-lookup"><span data-stu-id="8cc64-118">-Key</span></span>
<span data-ttu-id="8cc64-119">Schlüssel der Anreicherung</span><span class="sxs-lookup"><span data-stu-id="8cc64-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="8cc64-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8cc64-120">-Name</span></span>
<span data-ttu-id="8cc64-121">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="8cc64-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8cc64-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cc64-122">-PassThru</span></span>
<span data-ttu-id="8cc64-123">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="8cc64-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="8cc64-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8cc64-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cc64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc64-125">-ResourceGroupName</span></span>
<span data-ttu-id="8cc64-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8cc64-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8cc64-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cc64-127">-ResourceId</span></span>
<span data-ttu-id="8cc64-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8cc64-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8cc64-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cc64-129">-Confirm</span></span>
<span data-ttu-id="8cc64-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cc64-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc64-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8cc64-131">-WhatIf</span></span>
<span data-ttu-id="8cc64-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cc64-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc64-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cc64-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc64-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc64-134">CommonParameters</span></span>
<span data-ttu-id="8cc64-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc64-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc64-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc64-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc64-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8cc64-137">INPUTS</span></span>

### <span data-ttu-id="8cc64-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8cc64-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8cc64-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8cc64-139">System.String</span></span>

## <span data-ttu-id="8cc64-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8cc64-140">OUTPUTS</span></span>

### <span data-ttu-id="8cc64-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8cc64-141">System.Boolean</span></span>

## <span data-ttu-id="8cc64-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8cc64-142">NOTES</span></span>

## <span data-ttu-id="8cc64-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8cc64-143">RELATED LINKS</span></span>
