---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664230"
---
# <span data-ttu-id="4dfb7-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4dfb7-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="4dfb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dfb7-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfb7-103">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="4dfb7-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dfb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dfb7-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dfb7-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dfb7-105">EXAMPLES</span></span>

### <span data-ttu-id="4dfb7-106">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4dfb7-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="4dfb7-107">Erstellt die Consumer-Gruppe \` MyConsumerGroupName \` im Ereignis \` -Hub \` -MyEventHubName mit dem Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4dfb7-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4dfb7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dfb7-108">PARAMETERS</span></span>

### <span data-ttu-id="4dfb7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfb7-109">-DefaultProfile</span></span>
<span data-ttu-id="4dfb7-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4dfb7-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfb7-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4dfb7-111">-EventHub</span></span>
<span data-ttu-id="4dfb7-112">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="4dfb7-112">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfb7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4dfb7-113">-Name</span></span>
<span data-ttu-id="4dfb7-114">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="4dfb7-114">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfb7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4dfb7-115">-Namespace</span></span>
<span data-ttu-id="4dfb7-116">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4dfb7-116">Namespace Name</span></span>

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

### <span data-ttu-id="4dfb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dfb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="4dfb7-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4dfb7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4dfb7-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4dfb7-119">-UserMetadata</span></span>
<span data-ttu-id="4dfb7-120">Benutzer Metadaten für consumergroup</span><span class="sxs-lookup"><span data-stu-id="4dfb7-120">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfb7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4dfb7-121">-Confirm</span></span>
<span data-ttu-id="4dfb7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dfb7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfb7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfb7-123">-WhatIf</span></span>
<span data-ttu-id="4dfb7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dfb7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dfb7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dfb7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfb7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfb7-126">CommonParameters</span></span>
<span data-ttu-id="4dfb7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfb7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4dfb7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dfb7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfb7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dfb7-129">INPUTS</span></span>

### <span data-ttu-id="4dfb7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4dfb7-130">System.String</span></span>


## <span data-ttu-id="4dfb7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dfb7-131">OUTPUTS</span></span>

### <span data-ttu-id="4dfb7-132">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="4dfb7-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="4dfb7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dfb7-133">NOTES</span></span>

## <span data-ttu-id="4dfb7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dfb7-134">RELATED LINKS</span></span>
