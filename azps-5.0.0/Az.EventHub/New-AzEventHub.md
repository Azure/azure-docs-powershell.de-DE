---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179282"
---
# <span data-ttu-id="31853-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="31853-101">New-AzEventHub</span></span>

## <span data-ttu-id="31853-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31853-102">SYNOPSIS</span></span>
<span data-ttu-id="31853-103">Erstellt einen neuen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="31853-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="31853-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31853-104">SYNTAX</span></span>

### <span data-ttu-id="31853-105">EventhubPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="31853-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31853-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31853-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31853-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31853-107">DESCRIPTION</span></span>
<span data-ttu-id="31853-108">Das New-AzEventHub-Cmdlet erstellt einen neuen Azure Event-Hub.</span><span class="sxs-lookup"><span data-stu-id="31853-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="31853-109">Führen Sie die folgenden Schritte aus, um Eventhub mit Capture Description-Eigenschaften zu erstellen (Beispiele 2).</span><span class="sxs-lookup"><span data-stu-id="31853-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="31853-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31853-110">EXAMPLES</span></span>

### <span data-ttu-id="31853-111">Beispiel 1:-Erstellen eines neuen EventHub</span><span class="sxs-lookup"><span data-stu-id="31853-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="31853-112">Erstellt einen Ereignis-Hub mit dem Namen " \` MyEventHubName" \` mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten und zwei Partitionen an der \` westus- \` Position mit der Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="31853-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="31853-113">Beispiel 2: Aktualisieren von Eventhub mit "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="31853-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
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

<span data-ttu-id="31853-114">Erstellt einen Ereignis-Hub mit dem Namen \` MyEventHubName \` mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten, 2 Partitionen und CaptureDescription-Eigenschaften in der \` westus \` -Position mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="31853-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="31853-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="31853-115">PARAMETERS</span></span>

### <span data-ttu-id="31853-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31853-116">-DefaultProfile</span></span>
<span data-ttu-id="31853-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31853-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31853-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="31853-118">-InputObject</span></span>
<span data-ttu-id="31853-119">EventHub-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="31853-119">EventHub Input object</span></span>

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

### <span data-ttu-id="31853-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="31853-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="31853-121">Eventhub-Nachrichtenaufbewahrung in Tagen</span><span class="sxs-lookup"><span data-stu-id="31853-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="31853-122">-Name</span><span class="sxs-lookup"><span data-stu-id="31853-122">-Name</span></span>
<span data-ttu-id="31853-123">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="31853-123">Eventhub Name</span></span>

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

### <span data-ttu-id="31853-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="31853-124">-Namespace</span></span>
<span data-ttu-id="31853-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="31853-125">Namespace Name</span></span>

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

### <span data-ttu-id="31853-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="31853-126">-PartitionCount</span></span>
<span data-ttu-id="31853-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="31853-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="31853-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31853-128">-ResourceGroupName</span></span>
<span data-ttu-id="31853-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="31853-129">Resource Group Name</span></span>

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

### <span data-ttu-id="31853-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31853-130">-Confirm</span></span>
<span data-ttu-id="31853-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31853-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31853-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31853-132">-WhatIf</span></span>
<span data-ttu-id="31853-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31853-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31853-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31853-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31853-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31853-135">CommonParameters</span></span>
<span data-ttu-id="31853-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31853-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31853-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31853-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31853-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31853-138">INPUTS</span></span>

### <span data-ttu-id="31853-139">System. String</span><span class="sxs-lookup"><span data-stu-id="31853-139">System.String</span></span>

### <span data-ttu-id="31853-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="31853-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="31853-141">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="31853-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="31853-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31853-142">OUTPUTS</span></span>

### <span data-ttu-id="31853-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="31853-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="31853-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="31853-144">NOTES</span></span>

## <span data-ttu-id="31853-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31853-145">RELATED LINKS</span></span>
