---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372698"
---
# <span data-ttu-id="d862a-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d862a-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="d862a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d862a-102">SYNOPSIS</span></span>
<span data-ttu-id="d862a-103">Gibt eine Beschreibung für die angegebene Dienstbuswarteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="d862a-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="d862a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d862a-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d862a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d862a-105">DESCRIPTION</span></span>
<span data-ttu-id="d862a-106">Gibt eine Beschreibung für die angegebene Dienstbuswarteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="d862a-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="d862a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d862a-107">EXAMPLES</span></span>

### <span data-ttu-id="d862a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d862a-108">Example 1</span></span>
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

<span data-ttu-id="d862a-109">Gibt die Beschreibung der Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="d862a-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="d862a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d862a-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="d862a-111">Gibt eine Liste der Warteschlangen für den angegebenen Namespace zurück. Standardmäßig werden 100 Warteschlangen zurückgegeben, wenn mehr als 100 Warteschlangen zurückgegeben werden sollen, verwenden Sie den "-MaxCount"-Parameter.</span><span class="sxs-lookup"><span data-stu-id="d862a-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="d862a-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d862a-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="d862a-113">Gibt eine Liste der ersten 150 Warteschlangen für den angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="d862a-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="d862a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d862a-114">PARAMETERS</span></span>

### <span data-ttu-id="d862a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d862a-115">-DefaultProfile</span></span>
<span data-ttu-id="d862a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d862a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d862a-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d862a-117">-MaxCount</span></span>
<span data-ttu-id="d862a-118">Ermitteln Sie die maximale Anzahl der zurückzukehrenden Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="d862a-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="d862a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d862a-119">-Name</span></span>
<span data-ttu-id="d862a-120">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="d862a-120">Queue Name</span></span>

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

### <span data-ttu-id="d862a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d862a-121">-Namespace</span></span>
<span data-ttu-id="d862a-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="d862a-122">Namespace Name</span></span>

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

### <span data-ttu-id="d862a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d862a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d862a-124">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d862a-124">The name of the resource group</span></span>

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

### <span data-ttu-id="d862a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d862a-125">CommonParameters</span></span>
<span data-ttu-id="d862a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d862a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d862a-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d862a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d862a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d862a-128">INPUTS</span></span>

### <span data-ttu-id="d862a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d862a-129">System.String</span></span>

## <span data-ttu-id="d862a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d862a-130">OUTPUTS</span></span>

### <span data-ttu-id="d862a-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d862a-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="d862a-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d862a-132">NOTES</span></span>

## <span data-ttu-id="d862a-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d862a-133">RELATED LINKS</span></span>
