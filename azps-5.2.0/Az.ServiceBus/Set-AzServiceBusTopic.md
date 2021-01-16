---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360938"
---
# <span data-ttu-id="59a4c-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="59a4c-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="59a4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="59a4c-103">Aktualisiert die Beschreibung eines Dienstbusthemas im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="59a4c-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="59a4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59a4c-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59a4c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59a4c-105">DESCRIPTION</span></span>
<span data-ttu-id="59a4c-106">Das **Cmdlet "Set-AzServiceBusTopic"** aktualisiert ein Beschreibungsobjekt für ein Service Bus-Thema im angegebenen Namespace "Service Bus".</span><span class="sxs-lookup"><span data-stu-id="59a4c-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="59a4c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59a4c-107">EXAMPLES</span></span>

### <span data-ttu-id="59a4c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59a4c-108">Example 1</span></span>
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

<span data-ttu-id="59a4c-109">Aktualisiert das angegebene Thema mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="59a4c-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="59a4c-110">In diesem Beispiel wird die **Eigenschaft "EnableExpress"** auf **"true" aktualisiert.**</span><span class="sxs-lookup"><span data-stu-id="59a4c-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="59a4c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59a4c-111">PARAMETERS</span></span>

### <span data-ttu-id="59a4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a4c-112">-DefaultProfile</span></span>
<span data-ttu-id="59a4c-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a4c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59a4c-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59a4c-114">-InputObject</span></span>
<span data-ttu-id="59a4c-115">Definition des ServiceBus-Themas.</span><span class="sxs-lookup"><span data-stu-id="59a4c-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="59a4c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="59a4c-116">-Name</span></span>
<span data-ttu-id="59a4c-117">Themaname.</span><span class="sxs-lookup"><span data-stu-id="59a4c-117">Topic Name.</span></span>

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

### <span data-ttu-id="59a4c-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="59a4c-118">-Namespace</span></span>
<span data-ttu-id="59a4c-119">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="59a4c-119">Namespace Name.</span></span>

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

### <span data-ttu-id="59a4c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a4c-120">-ResourceGroupName</span></span>
<span data-ttu-id="59a4c-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="59a4c-121">The name of the resource group</span></span>

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

### <span data-ttu-id="59a4c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59a4c-122">-Confirm</span></span>
<span data-ttu-id="59a4c-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59a4c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a4c-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="59a4c-124">-WhatIf</span></span>
<span data-ttu-id="59a4c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59a4c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a4c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59a4c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a4c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a4c-127">CommonParameters</span></span>
<span data-ttu-id="59a4c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a4c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a4c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a4c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a4c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59a4c-130">INPUTS</span></span>

### <span data-ttu-id="59a4c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="59a4c-131">System.String</span></span>

### <span data-ttu-id="59a4c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="59a4c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="59a4c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59a4c-133">OUTPUTS</span></span>

### <span data-ttu-id="59a4c-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="59a4c-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="59a4c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59a4c-135">NOTES</span></span>

## <span data-ttu-id="59a4c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59a4c-136">RELATED LINKS</span></span>
