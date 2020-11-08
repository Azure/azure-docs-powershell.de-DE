---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178919"
---
# <span data-ttu-id="004be-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="004be-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="004be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="004be-102">SYNOPSIS</span></span>
<span data-ttu-id="004be-103">Erstellt eine neue Azure-Ereignis Raster Domäne.</span><span class="sxs-lookup"><span data-stu-id="004be-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="004be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="004be-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="004be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="004be-105">DESCRIPTION</span></span>
<span data-ttu-id="004be-106">Erstellt eine neue Azure-Ereignis Raster Domäne.</span><span class="sxs-lookup"><span data-stu-id="004be-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="004be-107">Nachdem die Domäne erstellt wurde, kann eine Anwendung Ereignisse für den Themen Endpunkt veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="004be-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="004be-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="004be-108">EXAMPLES</span></span>

### <span data-ttu-id="004be-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="004be-109">Example 1</span></span>

<span data-ttu-id="004be-110">Erstellt eine Ereignis Raster \` -Domänen domain1 \` im angegebenen geografischen Standort \` westus2 in der \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="004be-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="004be-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="004be-111">Example 2</span></span>

<span data-ttu-id="004be-112">Erstellt eine Ereignis Raster \` -Domänen domain1 am \` angegebenen geografischen Standort \` westus2 in der \` Ressourcengruppe \` MyResourceGroupName \` mit den angegebenen Tags "Department" und "Environment".</span><span class="sxs-lookup"><span data-stu-id="004be-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="004be-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="004be-113">PARAMETERS</span></span>

### <span data-ttu-id="004be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004be-114">-DefaultProfile</span></span>
<span data-ttu-id="004be-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="004be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="004be-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="004be-116">-InboundIpRule</span></span>
<span data-ttu-id="004be-117">Hashtable, die eine Liste der eingehenden IP-Regeln darstellt.</span><span class="sxs-lookup"><span data-stu-id="004be-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="004be-118">Jede Regel gibt die IP-Adresse in der CIDR-Notation an, beispielsweise 10.0.0.0/8 zusammen mit der entsprechenden Aktion, die auf der Grundlage der Übereinstimmung oder keine Übereinstimmung des IpMask durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="004be-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="004be-119">Mögliche Aktionswerte sind "nur zulassen"</span><span class="sxs-lookup"><span data-stu-id="004be-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="004be-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="004be-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="004be-121">Hashtable, die die Eingabe Zuordnungsfelder mit dem Standardwert im Leerzeichen getrennten Schlüssel = Wert Format darstellt.</span><span class="sxs-lookup"><span data-stu-id="004be-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="004be-122">Zulässige Schlüsselnamen sind: subject, EventType und dataversion.</span><span class="sxs-lookup"><span data-stu-id="004be-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="004be-123">Diese wird verwendet, wenn InputSchemaHelp nur customeventschema ist.</span><span class="sxs-lookup"><span data-stu-id="004be-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="004be-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="004be-124">-InputMappingField</span></span>
<span data-ttu-id="004be-125">Hashtable, die die Eingabe Zuordnungsfelder im Leerzeichen getrennten Schlüssel = Wert Format darstellt.</span><span class="sxs-lookup"><span data-stu-id="004be-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="004be-126">Zulässige Schlüsselnamen sind: ID, Topic, eventzeit, subject, EventType und dataversion.</span><span class="sxs-lookup"><span data-stu-id="004be-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="004be-127">Diese wird verwendet, wenn InputSchemaHelp nur customeventschema ist.</span><span class="sxs-lookup"><span data-stu-id="004be-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="004be-128">-Input Schema</span><span class="sxs-lookup"><span data-stu-id="004be-128">-InputSchema</span></span>
<span data-ttu-id="004be-129">Das Schema der Eingabeereignisse für das Thema.</span><span class="sxs-lookup"><span data-stu-id="004be-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="004be-130">Zulässige Werte sind: eventgridschema, customeventschema oder cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="004be-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="004be-131">Der Standardwert ist eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="004be-131">Default value is eventgridschema.</span></span> <span data-ttu-id="004be-132">Beachten Sie, dass bei Angabe von customeventschema auch InputMappingField-oder/und InputMappingDefaultValue-Parameter angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="004be-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="004be-133">-Standort</span><span class="sxs-lookup"><span data-stu-id="004be-133">-Location</span></span>
<span data-ttu-id="004be-134">Der Speicherort der Domäne.</span><span class="sxs-lookup"><span data-stu-id="004be-134">The location of the domain.</span></span>

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

### <span data-ttu-id="004be-135">-Name</span><span class="sxs-lookup"><span data-stu-id="004be-135">-Name</span></span>
<span data-ttu-id="004be-136">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="004be-136">EventGrid domain name.</span></span>

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

### <span data-ttu-id="004be-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="004be-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="004be-138">Dadurch wird festgelegt, ob Datenverkehr über öffentliches Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="004be-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="004be-139">Standardmäßig ist die Option aktiviert.</span><span class="sxs-lookup"><span data-stu-id="004be-139">By default it is enabled.</span></span> <span data-ttu-id="004be-140">Sie können den Zugriff auf bestimmte IPS weiter einschränken, indem Sie die InboundIpRule-Parameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="004be-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="004be-141">Zulässige Werte sind deaktiviert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="004be-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="004be-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004be-142">-ResourceGroupName</span></span>
<span data-ttu-id="004be-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="004be-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="004be-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="004be-144">-Tag</span></span>
<span data-ttu-id="004be-145">Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="004be-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="004be-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="004be-146">-Confirm</span></span>
<span data-ttu-id="004be-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="004be-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004be-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004be-148">-WhatIf</span></span>
<span data-ttu-id="004be-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="004be-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="004be-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="004be-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004be-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004be-151">CommonParameters</span></span>
<span data-ttu-id="004be-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004be-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004be-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="004be-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004be-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="004be-154">INPUTS</span></span>

### <span data-ttu-id="004be-155">System. String</span><span class="sxs-lookup"><span data-stu-id="004be-155">System.String</span></span>

### <span data-ttu-id="004be-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="004be-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="004be-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="004be-157">OUTPUTS</span></span>

### <span data-ttu-id="004be-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="004be-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="004be-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="004be-159">NOTES</span></span>

## <span data-ttu-id="004be-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="004be-160">RELATED LINKS</span></span>
