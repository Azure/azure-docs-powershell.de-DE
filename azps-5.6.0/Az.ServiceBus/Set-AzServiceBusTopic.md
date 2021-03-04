---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 9949757f82d6aa48d3981a10fa23eb32526dba8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937339"
---
# <span data-ttu-id="ec2dd-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ec2dd-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="ec2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2dd-103">Aktualisiert die Beschreibung eines Service Bus-Themas im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ec2dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec2dd-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec2dd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec2dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ec2dd-106">Das **Cmdlet Set-AzServiceBusTopic** aktualisiert ein Beschreibungsobjekt für ein Service Bus-Thema im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ec2dd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec2dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ec2dd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec2dd-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="ec2dd-109">Aktualisiert das angegebene Thema mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="ec2dd-110">In diesem Beispiel wird die **EnableExpress-Eigenschaft** auf **true aktualisiert.**</span><span class="sxs-lookup"><span data-stu-id="ec2dd-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="ec2dd-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec2dd-111">PARAMETERS</span></span>

### <span data-ttu-id="ec2dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2dd-112">-DefaultProfile</span></span>
<span data-ttu-id="ec2dd-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec2dd-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec2dd-114">-InputObject</span></span>
<span data-ttu-id="ec2dd-115">Definition des ServiceBus-Themas.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2dd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ec2dd-116">-Name</span></span>
<span data-ttu-id="ec2dd-117">Themaname.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-117">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2dd-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec2dd-118">-Namespace</span></span>
<span data-ttu-id="ec2dd-119">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-119">Namespace Name.</span></span>

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

### <span data-ttu-id="ec2dd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec2dd-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec2dd-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ec2dd-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ec2dd-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec2dd-122">-Confirm</span></span>
<span data-ttu-id="ec2dd-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec2dd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2dd-124">-WhatIf</span></span>
<span data-ttu-id="ec2dd-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec2dd-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec2dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2dd-127">CommonParameters</span></span>
<span data-ttu-id="ec2dd-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec2dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2dd-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec2dd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2dd-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec2dd-130">INPUTS</span></span>

### <span data-ttu-id="ec2dd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ec2dd-131">System.String</span></span>

### <span data-ttu-id="ec2dd-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ec2dd-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ec2dd-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec2dd-133">OUTPUTS</span></span>

### <span data-ttu-id="ec2dd-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ec2dd-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ec2dd-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec2dd-135">NOTES</span></span>

## <span data-ttu-id="ec2dd-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec2dd-136">RELATED LINKS</span></span>
