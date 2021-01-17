---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387021"
---
# <span data-ttu-id="a043c-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="a043c-101">New-AzEventHub</span></span>

## <span data-ttu-id="a043c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a043c-102">SYNOPSIS</span></span>
<span data-ttu-id="a043c-103">Erstellt einen neuen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="a043c-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="a043c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a043c-104">SYNTAX</span></span>

### <span data-ttu-id="a043c-105">EventhubPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a043c-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a043c-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a043c-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a043c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a043c-107">DESCRIPTION</span></span>
<span data-ttu-id="a043c-108">Das New-AzEventHub A0 erstellt einen neuen Azure-Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="a043c-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="a043c-109">Zum Erstellen von Eventhub mit Aufnahmebeschreibungseigenschaften führen Sie die folgenden Schritte aus (Beispiele 2).</span><span class="sxs-lookup"><span data-stu-id="a043c-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="a043c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a043c-110">EXAMPLES</span></span>

### <span data-ttu-id="a043c-111">Beispiel 1: – Erstellen eines neuen EventHub</span><span class="sxs-lookup"><span data-stu-id="a043c-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="a043c-112">Erstellt einen Ereignishub namens "MyEventHubName" mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten und zwei Partitionen am Speicherort "WestUS" mit der Ressourcengruppe \` \` \` \` \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="a043c-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a043c-113">Beispiel 2: Aktualisieren von Eventhub mit "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="a043c-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
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

<span data-ttu-id="a043c-114">Erstellt einen Ereignishub namens "MyEventHubName" mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten, zwei Partitionen und den Eigenschaften "CaptureDescription" am Speicherort "WestUS" mit der Ressourcengruppe \` \` \` \` \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="a043c-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a043c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a043c-115">PARAMETERS</span></span>

### <span data-ttu-id="a043c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a043c-116">-DefaultProfile</span></span>
<span data-ttu-id="a043c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a043c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a043c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a043c-118">-InputObject</span></span>
<span data-ttu-id="a043c-119">EventHub-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="a043c-119">EventHub Input object</span></span>

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

### <span data-ttu-id="a043c-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a043c-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="a043c-121">Aufbewahrung von Eventhub-Nachrichten in Tagen</span><span class="sxs-lookup"><span data-stu-id="a043c-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="a043c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a043c-122">-Name</span></span>
<span data-ttu-id="a043c-123">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="a043c-123">Eventhub Name</span></span>

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

### <span data-ttu-id="a043c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a043c-124">-Namespace</span></span>
<span data-ttu-id="a043c-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="a043c-125">Namespace Name</span></span>

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

### <span data-ttu-id="a043c-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a043c-126">-PartitionCount</span></span>
<span data-ttu-id="a043c-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a043c-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="a043c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a043c-128">-ResourceGroupName</span></span>
<span data-ttu-id="a043c-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a043c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="a043c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a043c-130">-Confirm</span></span>
<span data-ttu-id="a043c-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a043c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a043c-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a043c-132">-WhatIf</span></span>
<span data-ttu-id="a043c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a043c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a043c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a043c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a043c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a043c-135">CommonParameters</span></span>
<span data-ttu-id="a043c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a043c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a043c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a043c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a043c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a043c-138">INPUTS</span></span>

### <span data-ttu-id="a043c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a043c-139">System.String</span></span>

### <span data-ttu-id="a043c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a043c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="a043c-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a043c-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a043c-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a043c-142">OUTPUTS</span></span>

### <span data-ttu-id="a043c-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a043c-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="a043c-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a043c-144">NOTES</span></span>

## <span data-ttu-id="a043c-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a043c-145">RELATED LINKS</span></span>
