---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170670"
---
# <span data-ttu-id="81d9d-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="81d9d-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="81d9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="81d9d-103">Legt die Eigenschaften eines Themas "Veranstaltungsraster" fest.</span><span class="sxs-lookup"><span data-stu-id="81d9d-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="81d9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81d9d-104">SYNTAX</span></span>

### <span data-ttu-id="81d9d-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="81d9d-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d9d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d9d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81d9d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d9d-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81d9d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81d9d-108">DESCRIPTION</span></span>
<span data-ttu-id="81d9d-109">Legt die Eigenschaften eines Themas "Veranstaltungsraster" fest.</span><span class="sxs-lookup"><span data-stu-id="81d9d-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="81d9d-110">Dies kann verwendet werden, um die Tags eines Themas "Veranstaltungsraster" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="81d9d-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="81d9d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81d9d-111">EXAMPLES</span></span>

### <span data-ttu-id="81d9d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81d9d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="81d9d-113">Legt die Eigenschaften des Themas "Veranstaltungsraster" in der Ressourcengruppe "MyResourceGroupName" fest, um die Tags durch die angegebenen Tags \` \` \` \` "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="81d9d-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="81d9d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81d9d-114">PARAMETERS</span></span>

### <span data-ttu-id="81d9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d9d-115">-DefaultProfile</span></span>
<span data-ttu-id="81d9d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="81d9d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81d9d-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="81d9d-117">-InboundIpRule</span></span>
<span data-ttu-id="81d9d-118">Hashtable, die eine Liste der eingehenden #A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="81d9d-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="81d9d-119">Jede Regel gibt die IP-Adresse in der CIDR-Notation an, z. B. 10.0.0.0/8, zusammen mit der entsprechenden Aktion, die basierend auf der Übereinstimmung oder keiner Übereinstimmung des "IpMask" ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="81d9d-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="81d9d-120">Mögliche Aktionswerte umfassen "Nur zulassen"</span><span class="sxs-lookup"><span data-stu-id="81d9d-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="81d9d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81d9d-121">-InputObject</span></span>
<span data-ttu-id="81d9d-122">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="81d9d-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="81d9d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="81d9d-123">-Name</span></span>
<span data-ttu-id="81d9d-124">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="81d9d-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="81d9d-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="81d9d-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="81d9d-126">Dies bestimmt, ob Datenverkehr über das öffentliche Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="81d9d-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="81d9d-127">Standardmäßig ist sie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81d9d-127">By default it is enabled.</span></span> <span data-ttu-id="81d9d-128">Sie können weiter auf bestimmte IPs beschränken, indem Sie die Parameter für "InboundIpRule" konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="81d9d-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="81d9d-129">Zulässige Werte sind deaktiviert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="81d9d-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="81d9d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d9d-130">-ResourceGroupName</span></span>
<span data-ttu-id="81d9d-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="81d9d-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="81d9d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81d9d-132">-ResourceId</span></span>
<span data-ttu-id="81d9d-133">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="81d9d-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="81d9d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="81d9d-134">-Tag</span></span>
<span data-ttu-id="81d9d-135">Hashtables, die das Ressourcentag darstellt.</span><span class="sxs-lookup"><span data-stu-id="81d9d-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="81d9d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d9d-136">-Confirm</span></span>
<span data-ttu-id="81d9d-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81d9d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d9d-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="81d9d-138">-WhatIf</span></span>
<span data-ttu-id="81d9d-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81d9d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d9d-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81d9d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d9d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d9d-141">CommonParameters</span></span>
<span data-ttu-id="81d9d-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d9d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d9d-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81d9d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d9d-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81d9d-144">INPUTS</span></span>

### <span data-ttu-id="81d9d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="81d9d-145">System.String</span></span>

### <span data-ttu-id="81d9d-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="81d9d-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="81d9d-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="81d9d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81d9d-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81d9d-148">OUTPUTS</span></span>

### <span data-ttu-id="81d9d-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="81d9d-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="81d9d-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81d9d-150">NOTES</span></span>

## <span data-ttu-id="81d9d-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81d9d-151">RELATED LINKS</span></span>
