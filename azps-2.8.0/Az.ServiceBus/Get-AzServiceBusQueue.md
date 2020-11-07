---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 099e86e8ed085169823c40d51de376085f768753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823283"
---
# <span data-ttu-id="bd24e-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="bd24e-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="bd24e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd24e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd24e-103">Gibt eine Beschreibung für die angegebene ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="bd24e-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="bd24e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd24e-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd24e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd24e-105">DESCRIPTION</span></span>
<span data-ttu-id="bd24e-106">Gibt eine Beschreibung für die angegebene ServiceBus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="bd24e-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="bd24e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd24e-107">EXAMPLES</span></span>

### <span data-ttu-id="bd24e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd24e-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="bd24e-109">Gibt die Beschreibung der Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="bd24e-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="bd24e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bd24e-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="bd24e-111">Gibt die Liste der Warteschlangen für einen bestimmten Namespace zurück, standardmäßig werden 100-Warteschlangen zurückgegeben, wenn mehr als 100 Warteschlangen zurückgegeben werden, verwenden Sie bitte-MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd24e-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="bd24e-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bd24e-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="bd24e-113">Gibt die Liste der ersten 150-Warteschlangen für gegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="bd24e-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="bd24e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd24e-114">PARAMETERS</span></span>

### <span data-ttu-id="bd24e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd24e-115">-DefaultProfile</span></span>
<span data-ttu-id="bd24e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd24e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd24e-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bd24e-117">-MaxCount</span></span>
<span data-ttu-id="bd24e-118">Ermitteln Sie die maximale Anzahl von Warteschlangen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd24e-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd24e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bd24e-119">-Name</span></span>
<span data-ttu-id="bd24e-120">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="bd24e-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd24e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd24e-121">-Namespace</span></span>
<span data-ttu-id="bd24e-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="bd24e-122">Namespace Name</span></span>

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

### <span data-ttu-id="bd24e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd24e-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd24e-124">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bd24e-124">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd24e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd24e-125">CommonParameters</span></span>
<span data-ttu-id="bd24e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd24e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd24e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd24e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd24e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd24e-128">INPUTS</span></span>

### <span data-ttu-id="bd24e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bd24e-129">System.String</span></span>

## <span data-ttu-id="bd24e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd24e-130">OUTPUTS</span></span>

### <span data-ttu-id="bd24e-131">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="bd24e-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="bd24e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd24e-132">NOTES</span></span>

## <span data-ttu-id="bd24e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd24e-133">RELATED LINKS</span></span>
