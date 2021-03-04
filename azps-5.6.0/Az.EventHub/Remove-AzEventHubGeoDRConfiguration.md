---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2de5501c63ebbdd8842acb6cbfa40ec51893cbf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939560"
---
# <span data-ttu-id="a295c-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a295c-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="a295c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a295c-102">SYNOPSIS</span></span>
<span data-ttu-id="a295c-103">Löscht einen Alias(Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="a295c-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a295c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a295c-104">SYNTAX</span></span>

### <span data-ttu-id="a295c-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a295c-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a295c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a295c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a295c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a295c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a295c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a295c-108">DESCRIPTION</span></span>
<span data-ttu-id="a295c-109">Das **Cmdlet Remove-AzEventHubGeoDRConfiguration** löscht einen Alias(Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="a295c-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a295c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a295c-110">EXAMPLES</span></span>

### <span data-ttu-id="a295c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a295c-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="a295c-112">Löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="a295c-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a295c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a295c-113">PARAMETERS</span></span>

### <span data-ttu-id="a295c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a295c-114">-AsJob</span></span>
<span data-ttu-id="a295c-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a295c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a295c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a295c-116">-DefaultProfile</span></span>
<span data-ttu-id="a295c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a295c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a295c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a295c-118">-InputObject</span></span>
<span data-ttu-id="a295c-119">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="a295c-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a295c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a295c-120">-Name</span></span>
<span data-ttu-id="a295c-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="a295c-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="a295c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a295c-122">-Namespace</span></span>
<span data-ttu-id="a295c-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="a295c-123">Namespace Name</span></span>

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

### <span data-ttu-id="a295c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a295c-124">-PassThru</span></span>
<span data-ttu-id="a295c-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a295c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a295c-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a295c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a295c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a295c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a295c-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a295c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a295c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a295c-129">-ResourceId</span></span>
<span data-ttu-id="a295c-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="a295c-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a295c-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a295c-131">-Confirm</span></span>
<span data-ttu-id="a295c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a295c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a295c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a295c-133">-WhatIf</span></span>
<span data-ttu-id="a295c-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a295c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a295c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a295c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a295c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a295c-136">CommonParameters</span></span>
<span data-ttu-id="a295c-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a295c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a295c-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a295c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a295c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a295c-139">INPUTS</span></span>

### <span data-ttu-id="a295c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a295c-140">System.String</span></span>

### <span data-ttu-id="a295c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a295c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="a295c-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a295c-142">OUTPUTS</span></span>

### <span data-ttu-id="a295c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a295c-143">System.Boolean</span></span>

## <span data-ttu-id="a295c-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a295c-144">NOTES</span></span>

## <span data-ttu-id="a295c-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a295c-145">RELATED LINKS</span></span>
