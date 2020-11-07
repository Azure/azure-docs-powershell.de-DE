---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 85f6373cad3c6c42bbefa0aba9aac14d3699b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662820"
---
# <span data-ttu-id="89744-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="89744-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="89744-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89744-102">SYNOPSIS</span></span>
<span data-ttu-id="89744-103">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="89744-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89744-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89744-104">SYNTAX</span></span>

### <span data-ttu-id="89744-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="89744-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89744-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89744-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89744-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89744-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89744-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89744-108">DESCRIPTION</span></span>
<span data-ttu-id="89744-109">Das Cmdlet **Remove-AzureRmEventHubGeoDRConfiguration** löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="89744-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="89744-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89744-110">EXAMPLES</span></span>

### <span data-ttu-id="89744-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89744-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="89744-112">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="89744-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="89744-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="89744-113">PARAMETERS</span></span>

### <span data-ttu-id="89744-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89744-114">-AsJob</span></span>
<span data-ttu-id="89744-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="89744-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89744-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89744-116">-DefaultProfile</span></span>
<span data-ttu-id="89744-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89744-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89744-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89744-118">-InputObject</span></span>
<span data-ttu-id="89744-119">Eventhub GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="89744-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89744-120">-Name</span><span class="sxs-lookup"><span data-stu-id="89744-120">-Name</span></span>
<span data-ttu-id="89744-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="89744-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89744-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89744-122">-Namespace</span></span>
<span data-ttu-id="89744-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="89744-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89744-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89744-124">-PassThru</span></span>
<span data-ttu-id="89744-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="89744-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89744-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="89744-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89744-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89744-127">-ResourceGroupName</span></span>
<span data-ttu-id="89744-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="89744-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89744-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="89744-129">-ResourceId</span></span>
<span data-ttu-id="89744-130">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="89744-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89744-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89744-131">-Confirm</span></span>
<span data-ttu-id="89744-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89744-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89744-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89744-133">-WhatIf</span></span>
<span data-ttu-id="89744-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89744-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89744-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89744-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89744-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89744-136">CommonParameters</span></span>
<span data-ttu-id="89744-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89744-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89744-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89744-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89744-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89744-139">INPUTS</span></span>

### <span data-ttu-id="89744-140">System. String</span><span class="sxs-lookup"><span data-stu-id="89744-140">System.String</span></span>

### <span data-ttu-id="89744-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="89744-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="89744-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89744-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="89744-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89744-143">OUTPUTS</span></span>

### <span data-ttu-id="89744-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89744-144">System.Boolean</span></span>

## <span data-ttu-id="89744-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="89744-145">NOTES</span></span>

## <span data-ttu-id="89744-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89744-146">RELATED LINKS</span></span>
