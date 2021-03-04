---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 9fe0fad7ec353b3805bb941b62f6f6b6ee83e157
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935776"
---
# <span data-ttu-id="6b9f6-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="6b9f6-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="6b9f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9f6-103">Legt die Eigenschaften eines Themas "Ereignisraster" fest.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="6b9f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b9f6-104">SYNTAX</span></span>

### <span data-ttu-id="6b9f6-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b9f6-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9f6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b9f6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b9f6-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b9f6-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b9f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b9f6-108">DESCRIPTION</span></span>
<span data-ttu-id="6b9f6-109">Legt die Eigenschaften eines Themas "Ereignisraster" fest.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="6b9f6-110">Dies kann verwendet werden, um die Tags eines Themas "Ereignisraster" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="6b9f6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b9f6-111">EXAMPLES</span></span>

### <span data-ttu-id="6b9f6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b9f6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="6b9f6-113">Legt die Eigenschaften des Themas "Event Grid Topic1" in der Ressourcengruppe MyResourceGroupName fest, um die Tags durch die angegebenen Tags \` \` \` \` "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="6b9f6-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b9f6-114">PARAMETERS</span></span>

### <span data-ttu-id="6b9f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9f6-115">-DefaultProfile</span></span>
<span data-ttu-id="6b9f6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6b9f6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b9f6-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="6b9f6-117">-InboundIpRule</span></span>
<span data-ttu-id="6b9f6-118">Hashtable, die eine Liste der eingehenden #A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="6b9f6-119">Jede Regel gibt die IP-Adresse in der CIDR-Notation an, z. B. 10.0.0.0/8 zusammen mit der entsprechenden Aktion, die basierend auf der Übereinstimmung oder keiner Übereinstimmung der IpMask ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="6b9f6-120">Mögliche Aktionswerte umfassen Nur zulassen</span><span class="sxs-lookup"><span data-stu-id="6b9f6-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b9f6-121">-InputObject</span></span>
<span data-ttu-id="6b9f6-122">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6b9f6-123">-Name</span></span>
<span data-ttu-id="6b9f6-124">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6b9f6-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="6b9f6-126">Dadurch wird bestimmt, ob Datenverkehr über das öffentliche Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="6b9f6-127">Standardmäßig ist es aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-127">By default it is enabled.</span></span> <span data-ttu-id="6b9f6-128">Sie können weitere Beschränkungen auf bestimmte IPs durch Konfigurieren von InboundIpRule-Parametern festlegen.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="6b9f6-129">Zulässige Werte sind deaktiviert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b9f6-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b9f6-132">-ResourceId</span></span>
<span data-ttu-id="6b9f6-133">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b9f6-134">-Tag</span></span>
<span data-ttu-id="6b9f6-135">Hashtables, die das Ressourcentag darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9f6-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b9f6-136">-Confirm</span></span>
<span data-ttu-id="6b9f6-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9f6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9f6-138">-WhatIf</span></span>
<span data-ttu-id="6b9f6-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9f6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9f6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9f6-141">CommonParameters</span></span>
<span data-ttu-id="6b9f6-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9f6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9f6-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b9f6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9f6-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b9f6-144">INPUTS</span></span>

### <span data-ttu-id="6b9f6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6b9f6-145">System.String</span></span>

### <span data-ttu-id="6b9f6-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="6b9f6-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="6b9f6-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b9f6-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b9f6-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b9f6-148">OUTPUTS</span></span>

### <span data-ttu-id="6b9f6-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="6b9f6-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="6b9f6-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b9f6-150">NOTES</span></span>

## <span data-ttu-id="6b9f6-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b9f6-151">RELATED LINKS</span></span>
