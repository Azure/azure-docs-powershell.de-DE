---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471850"
---
# <span data-ttu-id="fd231-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="fd231-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="fd231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd231-102">SYNOPSIS</span></span>
<span data-ttu-id="fd231-103">Aktualisiert eine Abonnementbeschreibung für ein Service bus-Thema im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="fd231-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fd231-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd231-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd231-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd231-105">DESCRIPTION</span></span>
<span data-ttu-id="fd231-106">Das **Cmdlet "Set-AzServiceBusSubscription"** aktualisiert die Beschreibung des Abonnements für das Thema "Service Bus" im angegebenen Namespace "Service Bus".</span><span class="sxs-lookup"><span data-stu-id="fd231-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fd231-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd231-107">EXAMPLES</span></span>

### <span data-ttu-id="fd231-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd231-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="fd231-109">Aktualisiert die Beschreibung für das angegebene Abonnement für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="fd231-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="fd231-110">In diesem Beispiel wird die **Eigenschaft "DeadLettringOnMessageExpiration"** auf **"true"** und **"MaxDeliveryCount"** auf "9" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fd231-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="fd231-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd231-111">PARAMETERS</span></span>

### <span data-ttu-id="fd231-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd231-112">-DefaultProfile</span></span>
<span data-ttu-id="fd231-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd231-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd231-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd231-114">-InputObject</span></span>
<span data-ttu-id="fd231-115">ServiceBus-Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="fd231-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd231-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd231-116">-Namespace</span></span>
<span data-ttu-id="fd231-117">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="fd231-117">Namespace Name.</span></span>

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

### <span data-ttu-id="fd231-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd231-118">-ResourceGroupName</span></span>
<span data-ttu-id="fd231-119">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fd231-119">The name of the resource group</span></span>

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

### <span data-ttu-id="fd231-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="fd231-120">-Topic</span></span>
<span data-ttu-id="fd231-121">Themaname.</span><span class="sxs-lookup"><span data-stu-id="fd231-121">Topic Name.</span></span>

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

### <span data-ttu-id="fd231-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd231-122">-Confirm</span></span>
<span data-ttu-id="fd231-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd231-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd231-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd231-124">-WhatIf</span></span>
<span data-ttu-id="fd231-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd231-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd231-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd231-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd231-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd231-127">CommonParameters</span></span>
<span data-ttu-id="fd231-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd231-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd231-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd231-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd231-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd231-130">INPUTS</span></span>

### <span data-ttu-id="fd231-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fd231-131">System.String</span></span>

### <span data-ttu-id="fd231-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="fd231-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="fd231-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd231-133">OUTPUTS</span></span>

### <span data-ttu-id="fd231-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="fd231-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="fd231-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd231-135">NOTES</span></span>

## <span data-ttu-id="fd231-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd231-136">RELATED LINKS</span></span>
