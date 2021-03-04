---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 9d24a8f3355c885a610cf371f4fadb716c6b159e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938755"
---
# <span data-ttu-id="e0bba-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e0bba-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="e0bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bba-103">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e0bba-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="e0bba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0bba-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0bba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0bba-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bba-106">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e0bba-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="e0bba-107">Nachdem die Domäne erstellt wurde, kann eine Anwendung Ereignisse auf dem Themenendpunkt veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e0bba-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="e0bba-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0bba-108">EXAMPLES</span></span>

### <span data-ttu-id="e0bba-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0bba-109">Example 1</span></span>

<span data-ttu-id="e0bba-110">Erstellt eine Ereignisrasterdomäne Domäne1 am angegebenen \` \` geografischen Standort \` westus2 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e0bba-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="e0bba-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e0bba-111">Example 2</span></span>

<span data-ttu-id="e0bba-112">Erstellt eine Ereignisrasterdomäne Domäne1 am angegebenen geografischen Standort westus2 in der Ressourcengruppe MyResourceGroupName mit den angegebenen Tags \` \` \` \` \` \` "Department" und "Environment".</span><span class="sxs-lookup"><span data-stu-id="e0bba-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="e0bba-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0bba-113">PARAMETERS</span></span>

### <span data-ttu-id="e0bba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bba-114">-DefaultProfile</span></span>
<span data-ttu-id="e0bba-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0bba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0bba-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="e0bba-116">-InboundIpRule</span></span>
<span data-ttu-id="e0bba-117">Hashtable, die eine Liste der eingehenden #A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0bba-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="e0bba-118">Jede Regel gibt die IP-Adresse in der CIDR-Notation an, z. B. 10.0.0.0/8 zusammen mit der entsprechenden Aktion, die basierend auf der Übereinstimmung oder keiner Übereinstimmung der IpMask ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0bba-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="e0bba-119">Mögliche Aktionswerte umfassen Nur zulassen</span><span class="sxs-lookup"><span data-stu-id="e0bba-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="e0bba-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="e0bba-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="e0bba-121">Hashtable, die die Eingabezuordnungsfelder mit dem Standardwert im Leerzeichen getrennten Schlüssel = Wertformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0bba-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="e0bba-122">Zulässige Schlüsselnamen sind: Betreff, Ereignistyp und Datenversion.</span><span class="sxs-lookup"><span data-stu-id="e0bba-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="e0bba-123">Dies wird verwendet, wenn InputSchemaHelp nur customeventschema ist.</span><span class="sxs-lookup"><span data-stu-id="e0bba-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="e0bba-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="e0bba-124">-InputMappingField</span></span>
<span data-ttu-id="e0bba-125">Hashtable, die die Eingabezuordnungsfelder im Leerzeichen getrennten Schlüssel = Wertformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0bba-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="e0bba-126">Zulässige Schlüsselnamen sind: ID, Thema, Ereigniszeit, Betreff, Ereignistyp und Datenversion.</span><span class="sxs-lookup"><span data-stu-id="e0bba-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="e0bba-127">Dies wird verwendet, wenn InputSchemaHelp nur customeventschema ist.</span><span class="sxs-lookup"><span data-stu-id="e0bba-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="e0bba-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="e0bba-128">-InputSchema</span></span>
<span data-ttu-id="e0bba-129">Das Schema der Eingabeereignisse für das Thema.</span><span class="sxs-lookup"><span data-stu-id="e0bba-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="e0bba-130">Zulässige Werte sind: eventgridschema, customeventschema oder cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="e0bba-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="e0bba-131">Standardwert ist eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="e0bba-131">Default value is eventgridschema.</span></span> <span data-ttu-id="e0bba-132">Beachten Sie, dass bei Angabe von customeventschema auch die Parameter InputMappingField oder/und InputMappingDefaultValue angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e0bba-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="e0bba-133">-Location</span><span class="sxs-lookup"><span data-stu-id="e0bba-133">-Location</span></span>
<span data-ttu-id="e0bba-134">Der Speicherort der Domäne.</span><span class="sxs-lookup"><span data-stu-id="e0bba-134">The location of the domain.</span></span>

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

### <span data-ttu-id="e0bba-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e0bba-135">-Name</span></span>
<span data-ttu-id="e0bba-136">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e0bba-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0bba-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e0bba-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="e0bba-138">Dadurch wird bestimmt, ob Datenverkehr über das öffentliche Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e0bba-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="e0bba-139">Standardmäßig ist es aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e0bba-139">By default it is enabled.</span></span> <span data-ttu-id="e0bba-140">Sie können weitere Beschränkungen auf bestimmte IPs durch Konfigurieren von InboundIpRule-Parametern festlegen.</span><span class="sxs-lookup"><span data-stu-id="e0bba-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="e0bba-141">Zulässige Werte sind deaktiviert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e0bba-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="e0bba-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0bba-142">-ResourceGroupName</span></span>
<span data-ttu-id="e0bba-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0bba-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0bba-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0bba-144">-Tag</span></span>
<span data-ttu-id="e0bba-145">Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0bba-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="e0bba-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0bba-146">-Confirm</span></span>
<span data-ttu-id="e0bba-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0bba-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0bba-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0bba-148">-WhatIf</span></span>
<span data-ttu-id="e0bba-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0bba-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0bba-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0bba-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0bba-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bba-151">CommonParameters</span></span>
<span data-ttu-id="e0bba-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0bba-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bba-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0bba-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bba-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0bba-154">INPUTS</span></span>

### <span data-ttu-id="e0bba-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e0bba-155">System.String</span></span>

### <span data-ttu-id="e0bba-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0bba-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0bba-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0bba-157">OUTPUTS</span></span>

### <span data-ttu-id="e0bba-158">Microsoft.Azure.Commands.EventGrid.Models.PSDOmain</span><span class="sxs-lookup"><span data-stu-id="e0bba-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="e0bba-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0bba-159">NOTES</span></span>

## <span data-ttu-id="e0bba-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0bba-160">RELATED LINKS</span></span>
