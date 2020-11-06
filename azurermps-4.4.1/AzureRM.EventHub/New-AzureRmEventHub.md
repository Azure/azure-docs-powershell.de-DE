---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505018"
---
# <span data-ttu-id="b638a-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="b638a-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="b638a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b638a-102">SYNOPSIS</span></span>
<span data-ttu-id="b638a-103">Erstellt einen neuen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="b638a-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b638a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b638a-104">SYNTAX</span></span>

### <span data-ttu-id="b638a-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b638a-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b638a-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b638a-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b638a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b638a-107">DESCRIPTION</span></span>
<span data-ttu-id="b638a-108">Das New-AzureRmEventHub-Cmdlet erstellt einen neuen Azure Event-Hub.</span><span class="sxs-lookup"><span data-stu-id="b638a-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="b638a-109">Führen Sie die folgenden Schritte aus, um Eventhub mit Capture Description-Eigenschaften zu erstellen (Beispiele 2).</span><span class="sxs-lookup"><span data-stu-id="b638a-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="b638a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b638a-110">EXAMPLES</span></span>

### <span data-ttu-id="b638a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b638a-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="b638a-112">Erstellt einen Ereignis-Hub mit dem Namen " \` MyEventHubName" \` mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten und zwei Partitionen an der \` westus- \` Position mit der Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b638a-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b638a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b638a-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="b638a-114">Erstellt einen Ereignis-Hub mit dem Namen \` MyEventHubName \` mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten, 2 Partitionen und CaptureDescription-Eigenschaften in der \` westus \` -Position mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b638a-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b638a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b638a-115">PARAMETERS</span></span>

### <span data-ttu-id="b638a-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="b638a-116">-Location</span></span>
<span data-ttu-id="b638a-117">Geographischer Speicherort des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="b638a-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b638a-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="b638a-119">Event Hubs-Nachrichten Aufbewahrungszeit in Tagen.</span><span class="sxs-lookup"><span data-stu-id="b638a-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b638a-120">-PartitionCount</span></span>
<span data-ttu-id="b638a-121">Die Anzahl von Partitionen im Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="b638a-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b638a-122">-ResourceGroupName</span></span>
<span data-ttu-id="b638a-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b638a-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b638a-124">-Confirm</span></span>
<span data-ttu-id="b638a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b638a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b638a-126">-WhatIf</span></span>
<span data-ttu-id="b638a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b638a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b638a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b638a-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b638a-129">-InputObject</span></span>
<span data-ttu-id="b638a-130">EventHub-Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="b638a-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b638a-131">-Name</span></span>
<span data-ttu-id="b638a-132">Eventhub-Name.</span><span class="sxs-lookup"><span data-stu-id="b638a-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b638a-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b638a-133">-Namespace</span></span>
<span data-ttu-id="b638a-134">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="b638a-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="b638a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b638a-135">INPUTS</span></span>

### <span data-ttu-id="b638a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b638a-136">System.String</span></span>

## <span data-ttu-id="b638a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b638a-137">OUTPUTS</span></span>

### <span data-ttu-id="b638a-138">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b638a-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="b638a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b638a-139">NOTES</span></span>

## <span data-ttu-id="b638a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b638a-140">RELATED LINKS</span></span>

