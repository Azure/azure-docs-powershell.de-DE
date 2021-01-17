---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302459"
---
# <span data-ttu-id="57a57-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="57a57-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="57a57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a57-102">SYNOPSIS</span></span>
<span data-ttu-id="57a57-103">Erstellen oder aktualisieren Sie den DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="57a57-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="57a57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57a57-104">SYNTAX</span></span>

### <span data-ttu-id="57a57-105">EventHub (Standard)</span><span class="sxs-lookup"><span data-stu-id="57a57-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57a57-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="57a57-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57a57-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57a57-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57a57-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57a57-108">DESCRIPTION</span></span>
<span data-ttu-id="57a57-109">Erstellen oder aktualisieren Sie den DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="57a57-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="57a57-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57a57-110">EXAMPLES</span></span>

### <span data-ttu-id="57a57-111">Beispiel 1: Erstellen eines AzDigitalTwinsEndpoint für Eventhub</span><span class="sxs-lookup"><span data-stu-id="57a57-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="57a57-112">Erstellen eines AzDigitalTwinsEndpoint für Eventhub durch connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="57a57-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="57a57-113">Beispiel 2: Erstellen eines AzDigitalTwinsEndpoint für EventGrid</span><span class="sxs-lookup"><span data-stu-id="57a57-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="57a57-114">Erstellen eines AzDigitalTwinsEndpoint für Eventhub nach TopicEndpoint und accessKey1</span><span class="sxs-lookup"><span data-stu-id="57a57-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="57a57-115">Beispiel 3: Erstellen eines AzDigitalTwinsEndpoint für ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57a57-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="57a57-116">Erstellen eines AzDigitalTwinsEndpoint fürServcBus von PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="57a57-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="57a57-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57a57-117">PARAMETERS</span></span>

### <span data-ttu-id="57a57-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="57a57-118">-AccessKey1</span></span>
<span data-ttu-id="57a57-119">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="57a57-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="57a57-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57a57-120">-AsJob</span></span>
<span data-ttu-id="57a57-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="57a57-121">Run the command as a job</span></span>

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

### <span data-ttu-id="57a57-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="57a57-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="57a57-123">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="57a57-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="57a57-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="57a57-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="57a57-125">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="57a57-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="57a57-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="57a57-126">-DeadLetterSecret</span></span>
<span data-ttu-id="57a57-127">Geheimer Speicher für in tote Briefe.</span><span class="sxs-lookup"><span data-stu-id="57a57-127">Dead letter storage secret.</span></span>
<span data-ttu-id="57a57-128">Wird während des Lesens verschleiert.</span><span class="sxs-lookup"><span data-stu-id="57a57-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="57a57-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a57-129">-DefaultProfile</span></span>
<span data-ttu-id="57a57-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57a57-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a57-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="57a57-131">-EndpointDescription</span></span>
<span data-ttu-id="57a57-132">Ressource für den DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="57a57-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="57a57-133">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu DEN ENDPOINTDESCRIPTION-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="57a57-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="57a57-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="57a57-134">-EndpointName</span></span>
<span data-ttu-id="57a57-135">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="57a57-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="57a57-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="57a57-136">-EndpointType</span></span>
<span data-ttu-id="57a57-137">Der Typ des DigitalEns-Endpunkts</span><span class="sxs-lookup"><span data-stu-id="57a57-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="57a57-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57a57-138">-NoWait</span></span>
<span data-ttu-id="57a57-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="57a57-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57a57-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="57a57-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="57a57-141">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="57a57-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="57a57-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a57-142">-ResourceGroupName</span></span>
<span data-ttu-id="57a57-143">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="57a57-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="57a57-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="57a57-144">-ResourceName</span></span>
<span data-ttu-id="57a57-145">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="57a57-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="57a57-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57a57-146">-SubscriptionId</span></span>
<span data-ttu-id="57a57-147">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="57a57-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="57a57-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="57a57-148">-TopicEndpoint</span></span>
<span data-ttu-id="57a57-149">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="57a57-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="57a57-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57a57-150">-Confirm</span></span>
<span data-ttu-id="57a57-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57a57-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a57-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="57a57-152">-WhatIf</span></span>
<span data-ttu-id="57a57-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57a57-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a57-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57a57-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a57-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a57-155">CommonParameters</span></span>
<span data-ttu-id="57a57-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a57-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a57-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57a57-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a57-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57a57-158">INPUTS</span></span>

### <span data-ttu-id="57a57-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="57a57-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="57a57-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57a57-160">OUTPUTS</span></span>

### <span data-ttu-id="57a57-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="57a57-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="57a57-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="57a57-162">NOTES</span></span>

<span data-ttu-id="57a57-163">ALIASE</span><span class="sxs-lookup"><span data-stu-id="57a57-163">ALIASES</span></span>

<span data-ttu-id="57a57-164">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="57a57-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57a57-165">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="57a57-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57a57-166">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57a57-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57a57-167">ENDPOINTDESCRIPTION: <IDigitalTwinsEndpointResource> Ressource des DigitalTwinsInstance-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="57a57-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="57a57-168">`EndpointType <EndpointType>`: Der Typ des DigitalEns-Endpunkts</span><span class="sxs-lookup"><span data-stu-id="57a57-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="57a57-169">`[DeadLetterSecret <String>]`: Geheimer Speicher für in tote Briefe.</span><span class="sxs-lookup"><span data-stu-id="57a57-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="57a57-170">Wird während des Lesens verschleiert.</span><span class="sxs-lookup"><span data-stu-id="57a57-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="57a57-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="57a57-171">RELATED LINKS</span></span>

