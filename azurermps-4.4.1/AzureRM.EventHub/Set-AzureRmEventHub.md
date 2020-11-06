---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500042"
---
# <span data-ttu-id="8a0e9-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="8a0e9-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="8a0e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0e9-103">Aktualisiert den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a0e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a0e9-104">SYNTAX</span></span>

### <span data-ttu-id="8a0e9-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a0e9-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8a0e9-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8a0e9-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8a0e9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a0e9-107">DESCRIPTION</span></span>
<span data-ttu-id="8a0e9-108">Das Set-AzureRmEventHub-Cmdlet aktualisiert die Eigenschaften des angegebenen Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="8a0e9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a0e9-109">EXAMPLES</span></span>

### <span data-ttu-id="8a0e9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a0e9-110">Example 1</span></span>
<span data-ttu-id="8a0e9-111">Führen Sie die folgenden Schritte aus, um Eventhub mit den Eigenschaften der Aufnahme Beschreibung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="8a0e9-112">Aktualisiert den vom \` \` MyCreatedEventHub-Objekt dargestellten MyEventHubName des Ereignis Hubs \` \` , wobei der Aufbewahrungszeitraum für die Nachricht auf 4 Tage, die Anzahl der Partitionen auf 2 und die CaptureDescription-Eigenschaften festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="8a0e9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8a0e9-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="8a0e9-114">Aktualisiert den vom \` \` MyCreatedEventHub-Objekt dargestellten MyEventHubName des Ereignis Hubs \` \` , wobei der Aufbewahrungszeitraum für die Nachricht auf 4 Tage und die Anzahl der Partitionen auf 2 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="8a0e9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a0e9-115">PARAMETERS</span></span>

### <span data-ttu-id="8a0e9-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8a0e9-116">-messageRetentionInDays</span></span>
<span data-ttu-id="8a0e9-117">Aufbewahrungszeitraum für Ereignis-Hub-Nachrichten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="8a0e9-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="8a0e9-118">-partitionCount</span></span>
<span data-ttu-id="8a0e9-119">Die Anzahl von Partitionen auf diesem Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="8a0e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a0e9-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-121">Resource group name.</span></span>

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

### <span data-ttu-id="8a0e9-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a0e9-122">-Confirm</span></span>
<span data-ttu-id="8a0e9-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a0e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a0e9-124">-WhatIf</span></span>
<span data-ttu-id="8a0e9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a0e9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a0e9-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a0e9-127">-InputObject</span></span>
<span data-ttu-id="8a0e9-128">EventHub-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-128">EventHub object.</span></span>

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

### <span data-ttu-id="8a0e9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8a0e9-129">-Name</span></span>
<span data-ttu-id="8a0e9-130">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-130">Namespace Name.</span></span>

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

### <span data-ttu-id="8a0e9-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8a0e9-131">-Namespace</span></span>
<span data-ttu-id="8a0e9-132">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8a0e9-132">Namespace Name.</span></span>

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

## <span data-ttu-id="8a0e9-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a0e9-133">INPUTS</span></span>

### <span data-ttu-id="8a0e9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8a0e9-134">System.String</span></span>

## <span data-ttu-id="8a0e9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a0e9-135">OUTPUTS</span></span>

### <span data-ttu-id="8a0e9-136">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8a0e9-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="8a0e9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a0e9-137">NOTES</span></span>

## <span data-ttu-id="8a0e9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a0e9-138">RELATED LINKS</span></span>

