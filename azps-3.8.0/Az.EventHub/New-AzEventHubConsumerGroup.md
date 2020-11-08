---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004306"
---
# <span data-ttu-id="e3702-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e3702-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="e3702-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3702-102">SYNOPSIS</span></span>
<span data-ttu-id="e3702-103">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="e3702-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e3702-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3702-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3702-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3702-105">DESCRIPTION</span></span>
<span data-ttu-id="e3702-106">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="e3702-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e3702-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3702-107">EXAMPLES</span></span>

### <span data-ttu-id="e3702-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3702-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="e3702-109">Erstellt die Consumer-Gruppe \` MyConsumerGroupName \` im Ereignis \` -Hub \` -MyEventHubName mit dem Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e3702-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e3702-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3702-110">PARAMETERS</span></span>

### <span data-ttu-id="e3702-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3702-111">-DefaultProfile</span></span>
<span data-ttu-id="e3702-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3702-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3702-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e3702-113">-EventHub</span></span>
<span data-ttu-id="e3702-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="e3702-114">EventHub Name</span></span>

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

### <span data-ttu-id="e3702-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e3702-115">-Name</span></span>
<span data-ttu-id="e3702-116">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="e3702-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="e3702-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e3702-117">-Namespace</span></span>
<span data-ttu-id="e3702-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e3702-118">Namespace Name</span></span>

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

### <span data-ttu-id="e3702-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3702-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3702-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e3702-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e3702-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e3702-121">-UserMetadata</span></span>
<span data-ttu-id="e3702-122">Benutzer Metadaten für consumergroup</span><span class="sxs-lookup"><span data-stu-id="e3702-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="e3702-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3702-123">-Confirm</span></span>
<span data-ttu-id="e3702-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3702-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3702-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3702-125">-WhatIf</span></span>
<span data-ttu-id="e3702-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3702-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3702-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3702-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3702-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3702-128">CommonParameters</span></span>
<span data-ttu-id="e3702-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3702-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3702-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3702-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3702-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3702-131">INPUTS</span></span>

### <span data-ttu-id="e3702-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e3702-132">System.String</span></span>

## <span data-ttu-id="e3702-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3702-133">OUTPUTS</span></span>

### <span data-ttu-id="e3702-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e3702-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="e3702-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3702-135">NOTES</span></span>

## <span data-ttu-id="e3702-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3702-136">RELATED LINKS</span></span>
