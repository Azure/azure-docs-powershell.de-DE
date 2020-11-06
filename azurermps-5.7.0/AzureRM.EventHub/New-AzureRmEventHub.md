---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502573"
---
# <span data-ttu-id="b90c5-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="b90c5-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="b90c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b90c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b90c5-103">Erstellt einen neuen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="b90c5-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b90c5-104">SYNTAX</span></span>

### <span data-ttu-id="b90c5-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b90c5-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b90c5-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b90c5-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b90c5-107">DESCRIPTION</span></span>
<span data-ttu-id="b90c5-108">Das New-AzureRmEventHub-Cmdlet erstellt einen neuen Azure Event-Hub.</span><span class="sxs-lookup"><span data-stu-id="b90c5-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="b90c5-109">Führen Sie die folgenden Schritte aus, um Eventhub mit Capture Description-Eigenschaften zu erstellen (Beispiele 2).</span><span class="sxs-lookup"><span data-stu-id="b90c5-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="b90c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b90c5-110">EXAMPLES</span></span>

### <span data-ttu-id="b90c5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b90c5-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="b90c5-112">Erstellt einen Ereignis-Hub mit dem Namen " \` MyEventHubName" \` mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten und zwei Partitionen an der \` westus- \` Position mit der Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b90c5-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b90c5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b90c5-113">Example 2</span></span>
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

<span data-ttu-id="b90c5-114">Erstellt einen Ereignis-Hub mit dem Namen \` MyEventHubName \` mit einem 3-tägigen Aufbewahrungszeitraum für Nachrichten, 2 Partitionen und CaptureDescription-Eigenschaften in der \` westus \` -Position mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b90c5-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b90c5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b90c5-115">PARAMETERS</span></span>

### <span data-ttu-id="b90c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90c5-116">-DefaultProfile</span></span>
<span data-ttu-id="b90c5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b90c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90c5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b90c5-118">-InputObject</span></span>
<span data-ttu-id="b90c5-119">EventHub-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="b90c5-119">EventHub Input object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90c5-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b90c5-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="b90c5-121">Eventhub-Nachrichtenaufbewahrung in Tagen</span><span class="sxs-lookup"><span data-stu-id="b90c5-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="b90c5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b90c5-122">-Name</span></span>
<span data-ttu-id="b90c5-123">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="b90c5-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90c5-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b90c5-124">-Namespace</span></span>
<span data-ttu-id="b90c5-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="b90c5-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90c5-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b90c5-126">-PartitionCount</span></span>
<span data-ttu-id="b90c5-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b90c5-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="b90c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="b90c5-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b90c5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b90c5-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b90c5-130">-Confirm</span></span>
<span data-ttu-id="b90c5-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b90c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90c5-132">-WhatIf</span></span>
<span data-ttu-id="b90c5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b90c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90c5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b90c5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90c5-135">CommonParameters</span></span>
<span data-ttu-id="b90c5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b90c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b90c5-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90c5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90c5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b90c5-138">INPUTS</span></span>

### <span data-ttu-id="b90c5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b90c5-139">System.String</span></span>
<span data-ttu-id="b90c5-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b90c5-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="b90c5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b90c5-141">OUTPUTS</span></span>

### <span data-ttu-id="b90c5-142">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b90c5-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="b90c5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b90c5-143">NOTES</span></span>

## <span data-ttu-id="b90c5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b90c5-144">RELATED LINKS</span></span>
