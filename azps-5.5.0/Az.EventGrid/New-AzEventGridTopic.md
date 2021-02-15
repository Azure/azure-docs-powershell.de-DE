---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155729"
---
# <span data-ttu-id="71a2a-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="71a2a-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="71a2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="71a2a-103">Erstellt ein neues Azure-Veranstaltungsrasterthema.</span><span class="sxs-lookup"><span data-stu-id="71a2a-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="71a2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71a2a-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a2a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="71a2a-106">Erstellt ein neues Azure-Veranstaltungsrasterthema.</span><span class="sxs-lookup"><span data-stu-id="71a2a-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="71a2a-107">Nachdem das Thema erstellt wurde, kann eine Anwendung Ereignisse am Themenendpunkt veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="71a2a-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="71a2a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71a2a-108">EXAMPLES</span></span>

### <span data-ttu-id="71a2a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71a2a-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="71a2a-110">Erstellt ein Ereignisrasterthema "Topic1" am angegebenen geografischen Standort \` \` \` "westus2" \` in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="71a2a-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="71a2a-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="71a2a-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="71a2a-112">Erstellt ein Ereignisrasterthema "Topic1" am angegebenen geografischen Standort "westus2" in der Ressourcengruppe \` \` \` \` "MyResourceGroupName" mit den angegebenen Tags \` \` "Department" und "Environment".</span><span class="sxs-lookup"><span data-stu-id="71a2a-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="71a2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71a2a-113">PARAMETERS</span></span>

### <span data-ttu-id="71a2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a2a-114">-DefaultProfile</span></span>
<span data-ttu-id="71a2a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="71a2a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71a2a-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="71a2a-116">-InboundIpRule</span></span>
<span data-ttu-id="71a2a-117">Hashtable, die eine Liste der eingehenden #A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="71a2a-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="71a2a-118">Jede Regel gibt die IP-Adresse in der CIDR-Notation an, z. B. 10.0.0.0/8, zusammen mit der entsprechenden Aktion, die basierend auf der Übereinstimmung oder keiner Übereinstimmung des "IpMask" ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71a2a-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="71a2a-119">Mögliche Aktionswerte umfassen "Nur zulassen"</span><span class="sxs-lookup"><span data-stu-id="71a2a-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="71a2a-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="71a2a-121">Hashtable, die die Eingabezuordnungsfelder mit einem Standardwert im #A0 =Wertformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="71a2a-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="71a2a-122">Zulässige Schlüsselnamen sind: Betreff, Ereignistyp und Datenversion.</span><span class="sxs-lookup"><span data-stu-id="71a2a-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="71a2a-123">Dies wird verwendet, wenn InputSchemaHelp nur "customeventschema" ist.</span><span class="sxs-lookup"><span data-stu-id="71a2a-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="71a2a-124">-InputMappingField</span></span>
<span data-ttu-id="71a2a-125">Hashtable, die die Eingabezuordnungsfelder im Format "Leertaste = Wert" darstellt.</span><span class="sxs-lookup"><span data-stu-id="71a2a-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="71a2a-126">Zulässige Schlüsselnamen sind: id, topic, eventtime, subject, eventtype und dataversion.</span><span class="sxs-lookup"><span data-stu-id="71a2a-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="71a2a-127">Dies wird verwendet, wenn InputSchemaHelp nur "customeventschema" ist.</span><span class="sxs-lookup"><span data-stu-id="71a2a-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="71a2a-128">-InputSchema</span></span>
<span data-ttu-id="71a2a-129">Das Schema der Eingabeereignisse für das Thema.</span><span class="sxs-lookup"><span data-stu-id="71a2a-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="71a2a-130">Zulässige Werte sind: eventgridschema, customeventschema oder cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="71a2a-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="71a2a-131">Der Standardwert ist "eventgridschema".</span><span class="sxs-lookup"><span data-stu-id="71a2a-131">Default value is eventgridschema.</span></span> <span data-ttu-id="71a2a-132">Beachten Sie, dass bei Angabe von "customeventschema" auch die Parameter "InputMappingField" oder/und "InputMappingDefaultValue" angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="71a2a-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-133">-Location</span><span class="sxs-lookup"><span data-stu-id="71a2a-133">-Location</span></span>
<span data-ttu-id="71a2a-134">Der Speicherort des Themas</span><span class="sxs-lookup"><span data-stu-id="71a2a-134">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-135">-Name</span><span class="sxs-lookup"><span data-stu-id="71a2a-135">-Name</span></span>
<span data-ttu-id="71a2a-136">Der Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="71a2a-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="71a2a-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="71a2a-138">Dies bestimmt, ob Datenverkehr über ein öffentliches Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="71a2a-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="71a2a-139">Standardmäßig ist sie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="71a2a-139">By default it is enabled.</span></span> <span data-ttu-id="71a2a-140">Sie können weiter auf bestimmte IPs beschränken, indem Sie die Parameter für "InboundIpRule" konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="71a2a-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="71a2a-141">Zulässige Werte sind deaktiviert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="71a2a-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a2a-142">-ResourceGroupName</span></span>
<span data-ttu-id="71a2a-143">Die Ressourcengruppe, in der das Thema erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71a2a-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="71a2a-144">-Tag</span></span>
<span data-ttu-id="71a2a-145">Hashtables, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="71a2a-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a2a-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71a2a-146">-Confirm</span></span>
<span data-ttu-id="71a2a-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71a2a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a2a-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71a2a-148">-WhatIf</span></span>
<span data-ttu-id="71a2a-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71a2a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a2a-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71a2a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a2a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a2a-151">CommonParameters</span></span>
<span data-ttu-id="71a2a-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a2a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a2a-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71a2a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a2a-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71a2a-154">INPUTS</span></span>

### <span data-ttu-id="71a2a-155">System.String</span><span class="sxs-lookup"><span data-stu-id="71a2a-155">System.String</span></span>

### <span data-ttu-id="71a2a-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="71a2a-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="71a2a-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71a2a-157">OUTPUTS</span></span>

### <span data-ttu-id="71a2a-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="71a2a-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="71a2a-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71a2a-159">NOTES</span></span>

## <span data-ttu-id="71a2a-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71a2a-160">RELATED LINKS</span></span>
