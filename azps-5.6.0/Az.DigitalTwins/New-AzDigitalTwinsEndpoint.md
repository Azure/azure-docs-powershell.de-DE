---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935128"
---
# <span data-ttu-id="3272b-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3272b-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="3272b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3272b-102">SYNOPSIS</span></span>
<span data-ttu-id="3272b-103">Erstellen oder Aktualisieren des DigitalTwinsInstance-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3272b-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="3272b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3272b-104">SYNTAX</span></span>

### <span data-ttu-id="3272b-105">EventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="3272b-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3272b-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="3272b-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3272b-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3272b-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3272b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3272b-108">DESCRIPTION</span></span>
<span data-ttu-id="3272b-109">Erstellen oder Aktualisieren des DigitalTwinsInstance-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3272b-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="3272b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3272b-110">EXAMPLES</span></span>

### <span data-ttu-id="3272b-111">Beispiel 1: Erstellen eines AzDigitalTwinsEndpoints für Eventhub</span><span class="sxs-lookup"><span data-stu-id="3272b-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="3272b-112">Erstellen eines AzDigitalTwinsEndpoints für Eventhub durch connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="3272b-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="3272b-113">Beispiel 2: Erstellen eines AzDigitalTwinsEndpoints für EventGrid</span><span class="sxs-lookup"><span data-stu-id="3272b-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="3272b-114">Erstellen eines AzDigitalTwinsEndpoints für Eventhub nach TopicEndpoint und accessKey1</span><span class="sxs-lookup"><span data-stu-id="3272b-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="3272b-115">Beispiel 3: Erstellen eines AzDigitalTwinsEndpoints für ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3272b-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="3272b-116">Erstellen eines AzDigitalTwinsEndpoints für ServicBus von PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="3272b-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="3272b-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3272b-117">PARAMETERS</span></span>

### <span data-ttu-id="3272b-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="3272b-118">-AccessKey1</span></span>
<span data-ttu-id="3272b-119">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3272b-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3272b-120">-AsJob</span></span>
<span data-ttu-id="3272b-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3272b-121">Run the command as a job</span></span>

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

### <span data-ttu-id="3272b-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="3272b-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="3272b-123">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3272b-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="3272b-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="3272b-125">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3272b-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="3272b-126">-DeadLetterSecret</span></span>
<span data-ttu-id="3272b-127">Geheimer Speicher für "Toter Brief".</span><span class="sxs-lookup"><span data-stu-id="3272b-127">Dead letter storage secret.</span></span>
<span data-ttu-id="3272b-128">Wird während des Lesens verschleiert.</span><span class="sxs-lookup"><span data-stu-id="3272b-128">Will be obfuscated during read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3272b-129">-DefaultProfile</span></span>
<span data-ttu-id="3272b-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3272b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="3272b-131">-EndpointDescription</span></span>
<span data-ttu-id="3272b-132">DigitalTwinsInstance-Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="3272b-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="3272b-133">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für ENDPOINTDESCRIPTION-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3272b-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3272b-134">-EndpointName</span></span>
<span data-ttu-id="3272b-135">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="3272b-135">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3272b-136">-EndpointType</span></span>
<span data-ttu-id="3272b-137">Der Typ des Endpunkts "Digitale Partner"</span><span class="sxs-lookup"><span data-stu-id="3272b-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3272b-138">-NoWait</span></span>
<span data-ttu-id="3272b-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3272b-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3272b-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="3272b-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="3272b-141">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3272b-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3272b-142">-ResourceGroupName</span></span>
<span data-ttu-id="3272b-143">Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="3272b-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3272b-144">-ResourceName</span></span>
<span data-ttu-id="3272b-145">Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="3272b-145">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3272b-146">-SubscriptionId</span></span>
<span data-ttu-id="3272b-147">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3272b-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="3272b-148">-TopicEndpoint</span></span>
<span data-ttu-id="3272b-149">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3272b-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3272b-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3272b-150">-Confirm</span></span>
<span data-ttu-id="3272b-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3272b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3272b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3272b-152">-WhatIf</span></span>
<span data-ttu-id="3272b-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3272b-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3272b-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3272b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3272b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3272b-155">CommonParameters</span></span>
<span data-ttu-id="3272b-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3272b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3272b-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3272b-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3272b-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3272b-158">INPUTS</span></span>

### <span data-ttu-id="3272b-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="3272b-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="3272b-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3272b-160">OUTPUTS</span></span>

### <span data-ttu-id="3272b-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="3272b-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="3272b-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3272b-162">NOTES</span></span>

<span data-ttu-id="3272b-163">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3272b-163">ALIASES</span></span>

<span data-ttu-id="3272b-164">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3272b-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3272b-165">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="3272b-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3272b-166">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3272b-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3272b-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> : DigitalTwinsInstance-Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="3272b-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="3272b-168">`EndpointType <EndpointType>`: Der Typ des Endpunkts "Digitale Partner"</span><span class="sxs-lookup"><span data-stu-id="3272b-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="3272b-169">`[DeadLetterSecret <String>]`: Geheimer Aufbewahrungsgeheimnis für tote Briefe.</span><span class="sxs-lookup"><span data-stu-id="3272b-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="3272b-170">Wird während des Lesens verschleiert.</span><span class="sxs-lookup"><span data-stu-id="3272b-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="3272b-171">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3272b-171">RELATED LINKS</span></span>

