---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175665"
---
# <span data-ttu-id="5ecdc-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="5ecdc-101">Set-AzEventHub</span></span>

## <span data-ttu-id="5ecdc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ecdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5ecdc-103">Aktualisiert den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="5ecdc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ecdc-104">SYNTAX</span></span>

### <span data-ttu-id="5ecdc-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ecdc-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ecdc-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="5ecdc-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ecdc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ecdc-107">DESCRIPTION</span></span>
<span data-ttu-id="5ecdc-108">Das Set-AzEventHub-Cmdlet aktualisiert die Eigenschaften des angegebenen Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="5ecdc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ecdc-109">EXAMPLES</span></span>

### <span data-ttu-id="5ecdc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ecdc-110">Example 1</span></span>
<span data-ttu-id="5ecdc-111">Führen Sie die folgenden Schritte aus, um Eventhub mit den Eigenschaften der Aufnahme Beschreibung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="5ecdc-112">Aktualisiert den vom \` \` MyCreatedEventHub-Objekt dargestellten MyEventHubName des Ereignis Hubs \` \` , wobei der Aufbewahrungszeitraum für die Nachricht auf 4 Tage, die Anzahl der Partitionen auf 2 und die CaptureDescription-Eigenschaften festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="5ecdc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5ecdc-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="5ecdc-114">Aktualisiert den vom \` \` MyCreatedEventHub-Objekt dargestellten MyEventHubName des Ereignis Hubs \` \` , wobei der Aufbewahrungszeitraum für die Nachricht auf 4 Tage und die Anzahl der Partitionen auf 2 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="5ecdc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ecdc-115">PARAMETERS</span></span>

### <span data-ttu-id="5ecdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ecdc-116">-DefaultProfile</span></span>
<span data-ttu-id="5ecdc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ecdc-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ecdc-118">-InputObject</span></span>
<span data-ttu-id="5ecdc-119">EventHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="5ecdc-119">EventHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecdc-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5ecdc-120">-messageRetentionInDays</span></span>
<span data-ttu-id="5ecdc-121">Eventhub-Nachrichtenaufbewahrung in Tagen</span><span class="sxs-lookup"><span data-stu-id="5ecdc-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecdc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5ecdc-122">-Name</span></span>
<span data-ttu-id="5ecdc-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5ecdc-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecdc-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ecdc-124">-Namespace</span></span>
<span data-ttu-id="5ecdc-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5ecdc-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecdc-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="5ecdc-126">-partitionCount</span></span>
<span data-ttu-id="5ecdc-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="5ecdc-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecdc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ecdc-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ecdc-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5ecdc-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecdc-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ecdc-130">-Confirm</span></span>
<span data-ttu-id="5ecdc-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ecdc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ecdc-132">-WhatIf</span></span>
<span data-ttu-id="5ecdc-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ecdc-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ecdc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ecdc-135">CommonParameters</span></span>
<span data-ttu-id="5ecdc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ecdc-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ecdc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ecdc-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ecdc-138">INPUTS</span></span>

### <span data-ttu-id="5ecdc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5ecdc-139">System.String</span></span>

### <span data-ttu-id="5ecdc-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5ecdc-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="5ecdc-141">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ecdc-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5ecdc-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ecdc-142">OUTPUTS</span></span>

### <span data-ttu-id="5ecdc-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5ecdc-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="5ecdc-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ecdc-144">NOTES</span></span>

## <span data-ttu-id="5ecdc-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ecdc-145">RELATED LINKS</span></span>
