---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292402"
---
# <span data-ttu-id="27afb-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="27afb-101">Set-AzEventHub</span></span>

## <span data-ttu-id="27afb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27afb-102">SYNOPSIS</span></span>
<span data-ttu-id="27afb-103">Aktualisiert den angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="27afb-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="27afb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27afb-104">SYNTAX</span></span>

### <span data-ttu-id="27afb-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27afb-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27afb-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="27afb-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27afb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27afb-107">DESCRIPTION</span></span>
<span data-ttu-id="27afb-108">Das Set-AzEventHub cmdlet aktualisiert die Eigenschaften des angegebenen Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="27afb-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="27afb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27afb-109">EXAMPLES</span></span>

### <span data-ttu-id="27afb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27afb-110">Example 1</span></span>
<span data-ttu-id="27afb-111">Führen Sie die folgenden Schritte aus, um Eventhub mit den Eigenschaften der Aufnahmebeschreibung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="27afb-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

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

<span data-ttu-id="27afb-112">Aktualisiert den Vom \` MyEventHubName des \` MyCreatedEventHub-Objekts dargestellten Ereignishub, indem der Aufbewahrungszeitraum für Nachrichten auf 4 Tage, die Anzahl der Partitionen auf 2 und die \` \` Eigenschaften "CaptureDescription" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="27afb-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="27afb-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="27afb-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="27afb-114">Aktualisiert den Vom \` MyEventHubName des \` \` MyCreatedEventHub-Objekts dargestellten Ereignishub, indem der Aufbewahrungszeitraum für Nachrichten auf 4 Tage und die Anzahl der Partitionen auf \` 2 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="27afb-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="27afb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27afb-115">PARAMETERS</span></span>

### <span data-ttu-id="27afb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27afb-116">-DefaultProfile</span></span>
<span data-ttu-id="27afb-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27afb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27afb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27afb-118">-InputObject</span></span>
<span data-ttu-id="27afb-119">EventHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="27afb-119">EventHub object</span></span>

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

### <span data-ttu-id="27afb-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="27afb-120">-messageRetentionInDays</span></span>
<span data-ttu-id="27afb-121">Aufbewahrung von Eventhub-Nachrichten in Tagen</span><span class="sxs-lookup"><span data-stu-id="27afb-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="27afb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27afb-122">-Name</span></span>
<span data-ttu-id="27afb-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="27afb-123">Namespace Name</span></span>

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

### <span data-ttu-id="27afb-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27afb-124">-Namespace</span></span>
<span data-ttu-id="27afb-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="27afb-125">Namespace Name</span></span>

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

### <span data-ttu-id="27afb-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="27afb-126">-partitionCount</span></span>
<span data-ttu-id="27afb-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="27afb-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="27afb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27afb-128">-ResourceGroupName</span></span>
<span data-ttu-id="27afb-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="27afb-129">Resource Group Name</span></span>

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

### <span data-ttu-id="27afb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27afb-130">-Confirm</span></span>
<span data-ttu-id="27afb-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27afb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27afb-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27afb-132">-WhatIf</span></span>
<span data-ttu-id="27afb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27afb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27afb-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27afb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27afb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27afb-135">CommonParameters</span></span>
<span data-ttu-id="27afb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27afb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27afb-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27afb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27afb-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27afb-138">INPUTS</span></span>

### <span data-ttu-id="27afb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="27afb-139">System.String</span></span>

### <span data-ttu-id="27afb-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="27afb-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="27afb-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27afb-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="27afb-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27afb-142">OUTPUTS</span></span>

### <span data-ttu-id="27afb-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="27afb-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="27afb-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27afb-144">NOTES</span></span>

## <span data-ttu-id="27afb-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27afb-145">RELATED LINKS</span></span>
