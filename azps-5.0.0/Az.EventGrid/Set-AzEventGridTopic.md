---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177660"
---
# <span data-ttu-id="cc794-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="cc794-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="cc794-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc794-102">SYNOPSIS</span></span>
<span data-ttu-id="cc794-103">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="cc794-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="cc794-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc794-104">SYNTAX</span></span>

### <span data-ttu-id="cc794-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc794-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc794-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc794-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc794-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc794-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc794-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc794-108">DESCRIPTION</span></span>
<span data-ttu-id="cc794-109">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="cc794-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="cc794-110">Dies kann verwendet werden, um die Tags eines Ereignis Raster Themas zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="cc794-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="cc794-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc794-111">EXAMPLES</span></span>

### <span data-ttu-id="cc794-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc794-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="cc794-113">Legt die Eigenschaften des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName fest \` , um die Tags durch die angegebenen Tags "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="cc794-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="cc794-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc794-114">PARAMETERS</span></span>

### <span data-ttu-id="cc794-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc794-115">-DefaultProfile</span></span>
<span data-ttu-id="cc794-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cc794-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc794-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="cc794-117">-InboundIpRule</span></span>
<span data-ttu-id="cc794-118">Hashtable, die eine Liste der eingehenden IP-Regeln darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc794-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="cc794-119">Jede Regel gibt die IP-Adresse in der CIDR-Notation an, beispielsweise 10.0.0.0/8 zusammen mit der entsprechenden Aktion, die auf der Grundlage der Übereinstimmung oder keine Übereinstimmung des IpMask durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc794-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="cc794-120">Mögliche Aktionswerte sind "nur zulassen"</span><span class="sxs-lookup"><span data-stu-id="cc794-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="cc794-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc794-121">-InputObject</span></span>
<span data-ttu-id="cc794-122">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc794-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="cc794-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cc794-123">-Name</span></span>
<span data-ttu-id="cc794-124">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="cc794-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="cc794-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cc794-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="cc794-126">Dadurch wird festgelegt, ob Datenverkehr über öffentliches Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="cc794-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="cc794-127">Standardmäßig ist die Option aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cc794-127">By default it is enabled.</span></span> <span data-ttu-id="cc794-128">Sie können den Zugriff auf bestimmte IPS weiter einschränken, indem Sie die InboundIpRule-Parameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cc794-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="cc794-129">Zulässige Werte sind deaktiviert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cc794-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="cc794-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc794-130">-ResourceGroupName</span></span>
<span data-ttu-id="cc794-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc794-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="cc794-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc794-132">-ResourceId</span></span>
<span data-ttu-id="cc794-133">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="cc794-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="cc794-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc794-134">-Tag</span></span>
<span data-ttu-id="cc794-135">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="cc794-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="cc794-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc794-136">-Confirm</span></span>
<span data-ttu-id="cc794-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc794-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc794-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc794-138">-WhatIf</span></span>
<span data-ttu-id="cc794-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc794-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc794-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc794-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc794-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc794-141">CommonParameters</span></span>
<span data-ttu-id="cc794-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc794-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc794-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc794-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc794-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc794-144">INPUTS</span></span>

### <span data-ttu-id="cc794-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cc794-145">System.String</span></span>

### <span data-ttu-id="cc794-146">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="cc794-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="cc794-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc794-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cc794-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc794-148">OUTPUTS</span></span>

### <span data-ttu-id="cc794-149">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="cc794-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="cc794-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc794-150">NOTES</span></span>

## <span data-ttu-id="cc794-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc794-151">RELATED LINKS</span></span>
