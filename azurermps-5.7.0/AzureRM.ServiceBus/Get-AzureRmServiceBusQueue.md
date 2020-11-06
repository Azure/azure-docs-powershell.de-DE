---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480894"
---
# <span data-ttu-id="1f7d7-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="1f7d7-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="1f7d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7d7-103">Gibt eine Beschreibung für die angegebene ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f7d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f7d7-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f7d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f7d7-105">DESCRIPTION</span></span>
<span data-ttu-id="1f7d7-106">Das Cmdlet " **Get-AzureRmServiceBusQueue** " gibt eine Beschreibung der angegebenen ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="1f7d7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f7d7-107">EXAMPLES</span></span>

### <span data-ttu-id="1f7d7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1f7d7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="1f7d7-109">Gibt die Beschreibung der Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="1f7d7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f7d7-110">PARAMETERS</span></span>

### <span data-ttu-id="1f7d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7d7-111">-DefaultProfile</span></span>
<span data-ttu-id="1f7d7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f7d7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1f7d7-113">-Name</span></span>
<span data-ttu-id="1f7d7-114">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7d7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f7d7-115">-Namespace</span></span>
<span data-ttu-id="1f7d7-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-116">Namespace Name.</span></span>

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

### <span data-ttu-id="1f7d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f7d7-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1f7d7-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7d7-119">CommonParameters</span></span>
<span data-ttu-id="1f7d7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7d7-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7d7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7d7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f7d7-122">INPUTS</span></span>

### <span data-ttu-id="1f7d7-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f7d7-123">-ResourceGroup</span></span>
 <span data-ttu-id="1f7d7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1f7d7-124">System.String</span></span>
 

### <span data-ttu-id="1f7d7-125">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="1f7d7-125">-NamespaceName</span></span>
 <span data-ttu-id="1f7d7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1f7d7-126">System.String</span></span>
 

### <span data-ttu-id="1f7d7-127">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="1f7d7-127">-QueueName</span></span>
 <span data-ttu-id="1f7d7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1f7d7-128">System.String</span></span> 

## <span data-ttu-id="1f7d7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f7d7-129">OUTPUTS</span></span>

### <span data-ttu-id="1f7d7-130">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="1f7d7-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="1f7d7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f7d7-131">NOTES</span></span>

## <span data-ttu-id="1f7d7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f7d7-132">RELATED LINKS</span></span>

