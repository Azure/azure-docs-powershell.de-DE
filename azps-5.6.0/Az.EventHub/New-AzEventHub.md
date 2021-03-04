---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: 366bb4879b2db8bbb4a4335442a4abc6f07a5221
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921203"
---
# <span data-ttu-id="786ce-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="786ce-101">New-AzEventHub</span></span>

## <span data-ttu-id="786ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="786ce-102">SYNOPSIS</span></span>
<span data-ttu-id="786ce-103">Erstellt einen neuen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="786ce-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="786ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="786ce-104">SYNTAX</span></span>

### <span data-ttu-id="786ce-105">EventhubPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="786ce-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786ce-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="786ce-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="786ce-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="786ce-107">DESCRIPTION</span></span>
<span data-ttu-id="786ce-108">Das New-AzEventHub erstellt einen neuen Azure Event Hub.</span><span class="sxs-lookup"><span data-stu-id="786ce-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="786ce-109">Zum Erstellen von Eventhub mit Eigenschaften der Aufnahmebeschreibung führen Sie bitte die folgenden Schritte aus (Beispiele 2).</span><span class="sxs-lookup"><span data-stu-id="786ce-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="786ce-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="786ce-110">EXAMPLES</span></span>

### <span data-ttu-id="786ce-111">Beispiel 1: – Erstellen eines neuen EventHubs</span><span class="sxs-lookup"><span data-stu-id="786ce-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="786ce-112">Erstellt einen Ereignishub mit dem Namen MyEventHubName mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten und zwei Partitionen am WestUS-Speicherort mit der Ressourcengruppe \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="786ce-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="786ce-113">Beispiel 2: Aktualisieren von Eventhub mit "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="786ce-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="786ce-114">Erstellt einen Ereignishub mit dem Namen MyEventHubName mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten, zwei Partitionen und CaptureDescription-Eigenschaften am WestUS-Speicherort mit der Ressourcengruppe \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="786ce-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="786ce-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="786ce-115">PARAMETERS</span></span>

### <span data-ttu-id="786ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786ce-116">-DefaultProfile</span></span>
<span data-ttu-id="786ce-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="786ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="786ce-118">-InputObject</span></span>
<span data-ttu-id="786ce-119">EventHub-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="786ce-119">EventHub Input object</span></span>

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

### <span data-ttu-id="786ce-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="786ce-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="786ce-121">Ereignishub-Nachrichtenaufbewahrung in Tagen</span><span class="sxs-lookup"><span data-stu-id="786ce-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="786ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="786ce-122">-Name</span></span>
<span data-ttu-id="786ce-123">Eventhubname</span><span class="sxs-lookup"><span data-stu-id="786ce-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="786ce-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="786ce-124">-Namespace</span></span>
<span data-ttu-id="786ce-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="786ce-125">Namespace Name</span></span>

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

### <span data-ttu-id="786ce-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="786ce-126">-PartitionCount</span></span>
<span data-ttu-id="786ce-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="786ce-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="786ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="786ce-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="786ce-129">Resource Group Name</span></span>

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

### <span data-ttu-id="786ce-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="786ce-130">-Confirm</span></span>
<span data-ttu-id="786ce-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="786ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="786ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="786ce-132">-WhatIf</span></span>
<span data-ttu-id="786ce-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="786ce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="786ce-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="786ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="786ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786ce-135">CommonParameters</span></span>
<span data-ttu-id="786ce-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="786ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786ce-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="786ce-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786ce-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="786ce-138">INPUTS</span></span>

### <span data-ttu-id="786ce-139">System.String</span><span class="sxs-lookup"><span data-stu-id="786ce-139">System.String</span></span>

### <span data-ttu-id="786ce-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="786ce-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="786ce-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="786ce-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="786ce-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="786ce-142">OUTPUTS</span></span>

### <span data-ttu-id="786ce-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="786ce-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="786ce-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="786ce-144">NOTES</span></span>

## <span data-ttu-id="786ce-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="786ce-145">RELATED LINKS</span></span>
