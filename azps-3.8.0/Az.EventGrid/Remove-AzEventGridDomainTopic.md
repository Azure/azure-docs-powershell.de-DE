---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 2ca0c66490a95646ec3caa01b394b6210d472370
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996134"
---
# <span data-ttu-id="c4ea6-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c4ea6-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="c4ea6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ea6-103">Entfernt ein Azure-Ereignis Raster Domänen Thema.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="c4ea6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ea6-104">SYNTAX</span></span>

### <span data-ttu-id="c4ea6-105">DomainTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4ea6-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ea6-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4ea6-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ea6-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4ea6-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4ea6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="c4ea6-109">Entfernt ein Azure-Ereignis Raster Domänen Thema.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="c4ea6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="c4ea6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4ea6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="c4ea6-112">Entfernt die Ereignis Raster Domäne Topic \` THEMA1 hat \` Unterdomänen \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c4ea6-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c4ea6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c4ea6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="c4ea6-114">Entfernt die Ereignis Raster Domäne Topic \` THEMA1 hat \` Unterdomänen \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c4ea6-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c4ea6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ea6-115">PARAMETERS</span></span>

### <span data-ttu-id="c4ea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ea6-116">-DefaultProfile</span></span>
<span data-ttu-id="c4ea6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ea6-118">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="c4ea6-118">-DomainName</span></span>
<span data-ttu-id="c4ea6-119">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ea6-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4ea6-120">-InputObject</span></span>
<span data-ttu-id="c4ea6-121">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="c4ea6-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ea6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ea6-122">-Name</span></span>
<span data-ttu-id="c4ea6-123">EventGrid Domain Topic Name.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ea6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4ea6-124">-PassThru</span></span>
<span data-ttu-id="c4ea6-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c4ea6-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c4ea6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ea6-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4ea6-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ea6-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c4ea6-128">-ResourceId</span></span>
<span data-ttu-id="c4ea6-129">Ressourcenbezeichner, der das Thema der Ereignis Raster Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ea6-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4ea6-130">-Confirm</span></span>
<span data-ttu-id="c4ea6-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ea6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ea6-132">-WhatIf</span></span>
<span data-ttu-id="c4ea6-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ea6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ea6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ea6-135">CommonParameters</span></span>
<span data-ttu-id="c4ea6-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ea6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ea6-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ea6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ea6-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4ea6-138">INPUTS</span></span>

### <span data-ttu-id="c4ea6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4ea6-139">System.String</span></span>

### <span data-ttu-id="c4ea6-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c4ea6-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="c4ea6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4ea6-141">OUTPUTS</span></span>

### <span data-ttu-id="c4ea6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4ea6-142">System.Boolean</span></span>

## <span data-ttu-id="c4ea6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4ea6-143">NOTES</span></span>

## <span data-ttu-id="c4ea6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4ea6-144">RELATED LINKS</span></span>
