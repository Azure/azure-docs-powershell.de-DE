---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995788"
---
# <span data-ttu-id="25092-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="25092-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="25092-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25092-102">SYNOPSIS</span></span>
<span data-ttu-id="25092-103">Aktualisiert die Beschreibung einer Service Bus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="25092-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="25092-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25092-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25092-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25092-105">DESCRIPTION</span></span>
<span data-ttu-id="25092-106">Das Cmdlet " **Satz-AzServiceBusQueue** " aktualisiert die Beschreibung für die ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="25092-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="25092-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25092-107">EXAMPLES</span></span>

### <span data-ttu-id="25092-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25092-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
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
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="25092-109">Aktualisiert die angegebene Warteschlange mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="25092-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="25092-110">In diesem Beispiel wird die **DeadLetteringOnMessageExpiration** -Eigenschaft auf **true** und **SupportOrdering** auf **true** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="25092-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="25092-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="25092-111">PARAMETERS</span></span>

### <span data-ttu-id="25092-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25092-112">-DefaultProfile</span></span>
<span data-ttu-id="25092-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25092-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25092-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25092-114">-InputObject</span></span>
<span data-ttu-id="25092-115">ServiceBus-Definition.</span><span class="sxs-lookup"><span data-stu-id="25092-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25092-116">-Name</span><span class="sxs-lookup"><span data-stu-id="25092-116">-Name</span></span>
<span data-ttu-id="25092-117">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="25092-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25092-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25092-118">-Namespace</span></span>
<span data-ttu-id="25092-119">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="25092-119">Namespace Name.</span></span>

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

### <span data-ttu-id="25092-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25092-120">-ResourceGroupName</span></span>
<span data-ttu-id="25092-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="25092-121">The name of the resource group</span></span>

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

### <span data-ttu-id="25092-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25092-122">-Confirm</span></span>
<span data-ttu-id="25092-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25092-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25092-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25092-124">-WhatIf</span></span>
<span data-ttu-id="25092-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25092-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25092-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25092-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25092-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25092-127">CommonParameters</span></span>
<span data-ttu-id="25092-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25092-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25092-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25092-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25092-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25092-130">INPUTS</span></span>

### <span data-ttu-id="25092-131">System. String</span><span class="sxs-lookup"><span data-stu-id="25092-131">System.String</span></span>

### <span data-ttu-id="25092-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="25092-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="25092-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25092-133">OUTPUTS</span></span>

### <span data-ttu-id="25092-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="25092-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="25092-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="25092-135">NOTES</span></span>

## <span data-ttu-id="25092-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25092-136">RELATED LINKS</span></span>
