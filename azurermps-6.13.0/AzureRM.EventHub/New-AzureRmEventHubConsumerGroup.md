---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477838"
---
# <span data-ttu-id="945e0-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="945e0-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="945e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="945e0-102">SYNOPSIS</span></span>
<span data-ttu-id="945e0-103">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="945e0-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="945e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="945e0-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="945e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="945e0-105">DESCRIPTION</span></span>
<span data-ttu-id="945e0-106">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="945e0-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="945e0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="945e0-107">EXAMPLES</span></span>

### <span data-ttu-id="945e0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="945e0-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="945e0-109">Erstellt die Consumer-Gruppe \` MyConsumerGroupName \` im Ereignis \` -Hub \` -MyEventHubName mit dem Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="945e0-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="945e0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="945e0-110">PARAMETERS</span></span>

### <span data-ttu-id="945e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945e0-111">-DefaultProfile</span></span>
<span data-ttu-id="945e0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="945e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945e0-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="945e0-113">-EventHub</span></span>
<span data-ttu-id="945e0-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="945e0-114">EventHub Name</span></span>

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

### <span data-ttu-id="945e0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="945e0-115">-Name</span></span>
<span data-ttu-id="945e0-116">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="945e0-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945e0-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="945e0-117">-Namespace</span></span>
<span data-ttu-id="945e0-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="945e0-118">Namespace Name</span></span>

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

### <span data-ttu-id="945e0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945e0-119">-ResourceGroupName</span></span>
<span data-ttu-id="945e0-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="945e0-120">Resource Group Name</span></span>

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

### <span data-ttu-id="945e0-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="945e0-121">-UserMetadata</span></span>
<span data-ttu-id="945e0-122">Benutzer Metadaten für consumergroup</span><span class="sxs-lookup"><span data-stu-id="945e0-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945e0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="945e0-123">-Confirm</span></span>
<span data-ttu-id="945e0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="945e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="945e0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="945e0-125">-WhatIf</span></span>
<span data-ttu-id="945e0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="945e0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="945e0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="945e0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="945e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945e0-128">CommonParameters</span></span>
<span data-ttu-id="945e0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945e0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945e0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945e0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="945e0-131">INPUTS</span></span>

### <span data-ttu-id="945e0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="945e0-132">System.String</span></span>

## <span data-ttu-id="945e0-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="945e0-133">OUTPUTS</span></span>

### <span data-ttu-id="945e0-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="945e0-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="945e0-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="945e0-135">NOTES</span></span>

## <span data-ttu-id="945e0-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="945e0-136">RELATED LINKS</span></span>
