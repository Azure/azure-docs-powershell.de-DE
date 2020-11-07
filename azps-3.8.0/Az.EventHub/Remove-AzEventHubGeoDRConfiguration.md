---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845612"
---
# <span data-ttu-id="fe9a0-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe9a0-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="fe9a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9a0-103">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="fe9a0-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="fe9a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe9a0-104">SYNTAX</span></span>

### <span data-ttu-id="fe9a0-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe9a0-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9a0-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe9a0-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9a0-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe9a0-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe9a0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe9a0-108">DESCRIPTION</span></span>
<span data-ttu-id="fe9a0-109">Das Cmdlet **Remove-AzEventHubGeoDRConfiguration** löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="fe9a0-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="fe9a0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe9a0-110">EXAMPLES</span></span>

### <span data-ttu-id="fe9a0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe9a0-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="fe9a0-112">Löscht einen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="fe9a0-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="fe9a0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe9a0-113">PARAMETERS</span></span>

### <span data-ttu-id="fe9a0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe9a0-114">-AsJob</span></span>
<span data-ttu-id="fe9a0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fe9a0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe9a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9a0-116">-DefaultProfile</span></span>
<span data-ttu-id="fe9a0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe9a0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe9a0-118">-InputObject</span></span>
<span data-ttu-id="fe9a0-119">Eventhub GeoDR-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="fe9a0-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="fe9a0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fe9a0-120">-Name</span></span>
<span data-ttu-id="fe9a0-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="fe9a0-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="fe9a0-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fe9a0-122">-Namespace</span></span>
<span data-ttu-id="fe9a0-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fe9a0-123">Namespace Name</span></span>

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

### <span data-ttu-id="fe9a0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe9a0-124">-PassThru</span></span>
<span data-ttu-id="fe9a0-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe9a0-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe9a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe9a0-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fe9a0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="fe9a0-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fe9a0-129">-ResourceId</span></span>
<span data-ttu-id="fe9a0-130">GeoDRConfiguration-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fe9a0-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="fe9a0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe9a0-131">-Confirm</span></span>
<span data-ttu-id="fe9a0-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe9a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9a0-133">-WhatIf</span></span>
<span data-ttu-id="fe9a0-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe9a0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe9a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9a0-136">CommonParameters</span></span>
<span data-ttu-id="fe9a0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9a0-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9a0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9a0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe9a0-139">INPUTS</span></span>

### <span data-ttu-id="fe9a0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fe9a0-140">System.String</span></span>

### <span data-ttu-id="fe9a0-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fe9a0-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="fe9a0-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe9a0-142">OUTPUTS</span></span>

### <span data-ttu-id="fe9a0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe9a0-143">System.Boolean</span></span>

## <span data-ttu-id="fe9a0-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe9a0-144">NOTES</span></span>

## <span data-ttu-id="fe9a0-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe9a0-145">RELATED LINKS</span></span>
