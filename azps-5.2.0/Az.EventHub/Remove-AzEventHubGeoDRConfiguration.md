---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306536"
---
# <span data-ttu-id="ab7ed-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab7ed-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="ab7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7ed-103">Löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="ab7ed-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ab7ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab7ed-104">SYNTAX</span></span>

### <span data-ttu-id="ab7ed-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab7ed-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab7ed-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab7ed-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab7ed-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab7ed-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab7ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab7ed-108">DESCRIPTION</span></span>
<span data-ttu-id="ab7ed-109">Das **Cmdlet "Remove-AzEventHubGeoDRConfiguration"** löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="ab7ed-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ab7ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab7ed-110">EXAMPLES</span></span>

### <span data-ttu-id="ab7ed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab7ed-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="ab7ed-112">Löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="ab7ed-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ab7ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab7ed-113">PARAMETERS</span></span>

### <span data-ttu-id="ab7ed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab7ed-114">-AsJob</span></span>
<span data-ttu-id="ab7ed-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ab7ed-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab7ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7ed-116">-DefaultProfile</span></span>
<span data-ttu-id="ab7ed-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab7ed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab7ed-118">-InputObject</span></span>
<span data-ttu-id="ab7ed-119">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="ab7ed-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="ab7ed-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ab7ed-120">-Name</span></span>
<span data-ttu-id="ab7ed-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="ab7ed-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="ab7ed-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ab7ed-122">-Namespace</span></span>
<span data-ttu-id="ab7ed-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="ab7ed-123">Namespace Name</span></span>

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

### <span data-ttu-id="ab7ed-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab7ed-124">-PassThru</span></span>
<span data-ttu-id="ab7ed-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ab7ed-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ab7ed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab7ed-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab7ed-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ab7ed-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ab7ed-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab7ed-129">-ResourceId</span></span>
<span data-ttu-id="ab7ed-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="ab7ed-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="ab7ed-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab7ed-131">-Confirm</span></span>
<span data-ttu-id="ab7ed-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab7ed-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ab7ed-133">-WhatIf</span></span>
<span data-ttu-id="ab7ed-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab7ed-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab7ed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7ed-136">CommonParameters</span></span>
<span data-ttu-id="ab7ed-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab7ed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7ed-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab7ed-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7ed-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab7ed-139">INPUTS</span></span>

### <span data-ttu-id="ab7ed-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ab7ed-140">System.String</span></span>

### <span data-ttu-id="ab7ed-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ab7ed-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="ab7ed-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab7ed-142">OUTPUTS</span></span>

### <span data-ttu-id="ab7ed-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab7ed-143">System.Boolean</span></span>

## <span data-ttu-id="ab7ed-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab7ed-144">NOTES</span></span>

## <span data-ttu-id="ab7ed-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab7ed-145">RELATED LINKS</span></span>
