---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503958"
---
# <span data-ttu-id="00ec9-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="00ec9-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="00ec9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="00ec9-103">Gibt eine Beschreibung für die angegebene ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="00ec9-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00ec9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00ec9-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ec9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="00ec9-106">Das Cmdlet " **Get-AzureRmServiceBusQueue** " gibt eine Beschreibung der angegebenen ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="00ec9-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="00ec9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="00ec9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00ec9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="00ec9-109">Gibt die Beschreibung der Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="00ec9-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="00ec9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00ec9-110">PARAMETERS</span></span>

### <span data-ttu-id="00ec9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ec9-111">-DefaultProfile</span></span>
<span data-ttu-id="00ec9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00ec9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ec9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="00ec9-113">-Name</span></span>
<span data-ttu-id="00ec9-114">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="00ec9-114">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ec9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="00ec9-115">-Namespace</span></span>
<span data-ttu-id="00ec9-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="00ec9-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ec9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ec9-117">-ResourceGroupName</span></span>
<span data-ttu-id="00ec9-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="00ec9-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ec9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ec9-119">CommonParameters</span></span>
<span data-ttu-id="00ec9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ec9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ec9-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ec9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ec9-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00ec9-122">INPUTS</span></span>

### <span data-ttu-id="00ec9-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00ec9-123">-ResourceGroup</span></span>
 <span data-ttu-id="00ec9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="00ec9-124">System.String</span></span>
 

### <span data-ttu-id="00ec9-125">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="00ec9-125">-NamespaceName</span></span>
 <span data-ttu-id="00ec9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="00ec9-126">System.String</span></span>
 

### <span data-ttu-id="00ec9-127">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="00ec9-127">-QueueName</span></span>
 <span data-ttu-id="00ec9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00ec9-128">System.String</span></span> 

## <span data-ttu-id="00ec9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00ec9-129">OUTPUTS</span></span>

### <span data-ttu-id="00ec9-130">Microsoft. Azure. Commands. ServiceBus. Models. Queue Attributes</span><span class="sxs-lookup"><span data-stu-id="00ec9-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="00ec9-131">Lock Duration: AccessedAt: 1/1/0001 12:00:00 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 am DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: MessageCount CountDetails: ServiceBus: Microsoft. Azure. Management. MessageCountDetails-RequiresDuplicateDetection: false RequiresSession: Status: Active sizeInBytes: false 16384 SupportOrdering: 1/20/2017 2:51:37 am ID: UpdatedAt B-Queue_example1 Name: SB-Queue_example1 Typ: Microsoft./Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/Queues/S/Queues Location: West US</span><span class="sxs-lookup"><span data-stu-id="00ec9-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="00ec9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="00ec9-132">NOTES</span></span>

## <span data-ttu-id="00ec9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00ec9-133">RELATED LINKS</span></span>

