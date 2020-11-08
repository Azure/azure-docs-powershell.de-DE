---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175672"
---
# <span data-ttu-id="37990-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="37990-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="37990-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37990-102">SYNOPSIS</span></span>
<span data-ttu-id="37990-103">Entfernt ein Azure-Ereignis Raster Domänen Thema.</span><span class="sxs-lookup"><span data-stu-id="37990-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="37990-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37990-104">SYNTAX</span></span>

### <span data-ttu-id="37990-105">DomainTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="37990-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37990-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="37990-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37990-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37990-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37990-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37990-108">DESCRIPTION</span></span>
<span data-ttu-id="37990-109">Entfernt ein Azure-Ereignis Raster Domänen Thema.</span><span class="sxs-lookup"><span data-stu-id="37990-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="37990-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37990-110">EXAMPLES</span></span>

### <span data-ttu-id="37990-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37990-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="37990-112">Entfernt die Ereignis Raster Domäne Topic \` THEMA1 hat \` Unterdomänen \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="37990-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="37990-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="37990-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="37990-114">Entfernt die Ereignis Raster Domäne Topic \` THEMA1 hat \` Unterdomänen \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="37990-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="37990-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="37990-115">PARAMETERS</span></span>

### <span data-ttu-id="37990-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37990-116">-DefaultProfile</span></span>
<span data-ttu-id="37990-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37990-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37990-118">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="37990-118">-DomainName</span></span>
<span data-ttu-id="37990-119">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="37990-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="37990-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37990-120">-InputObject</span></span>
<span data-ttu-id="37990-121">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="37990-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="37990-122">-Name</span><span class="sxs-lookup"><span data-stu-id="37990-122">-Name</span></span>
<span data-ttu-id="37990-123">EventGrid Domain Topic Name.</span><span class="sxs-lookup"><span data-stu-id="37990-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="37990-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37990-124">-PassThru</span></span>
<span data-ttu-id="37990-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="37990-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="37990-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37990-126">-ResourceGroupName</span></span>
<span data-ttu-id="37990-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37990-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="37990-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="37990-128">-ResourceId</span></span>
<span data-ttu-id="37990-129">Ressourcenbezeichner, der das Thema der Ereignis Raster Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="37990-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="37990-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37990-130">-Confirm</span></span>
<span data-ttu-id="37990-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37990-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37990-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37990-132">-WhatIf</span></span>
<span data-ttu-id="37990-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37990-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37990-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37990-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37990-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37990-135">CommonParameters</span></span>
<span data-ttu-id="37990-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37990-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37990-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37990-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37990-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37990-138">INPUTS</span></span>

### <span data-ttu-id="37990-139">System. String</span><span class="sxs-lookup"><span data-stu-id="37990-139">System.String</span></span>

### <span data-ttu-id="37990-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="37990-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="37990-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37990-141">OUTPUTS</span></span>

### <span data-ttu-id="37990-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37990-142">System.Boolean</span></span>

## <span data-ttu-id="37990-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="37990-143">NOTES</span></span>

## <span data-ttu-id="37990-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37990-144">RELATED LINKS</span></span>
