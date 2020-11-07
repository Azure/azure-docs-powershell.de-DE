---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664720"
---
# <span data-ttu-id="ef1b2-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ef1b2-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="ef1b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1b2-103">Aktualisiert eine Abonnementbeschreibung für ein Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef1b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef1b2-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef1b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ef1b2-106">Das Cmdlet " **Satz-AzureRmServiceBusSubscription** " aktualisiert die Beschreibung des Abonnements für das ServiceBus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ef1b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef1b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ef1b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef1b2-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="ef1b2-109">Aktualisiert die Beschreibung des angegebenen Abonnements für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="ef1b2-110">In diesem Beispiel wird die **DeadLetteringOnMessageExpiration** -Eigenschaft auf **true** und **MaxDeliveryCount** auf 9 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="ef1b2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef1b2-111">PARAMETERS</span></span>

### <span data-ttu-id="ef1b2-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef1b2-112">-Confirm</span></span>
<span data-ttu-id="ef1b2-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1b2-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1b2-114">-WhatIf</span></span>
<span data-ttu-id="ef1b2-115">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef1b2-116">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1b2-117">-DefaultProfile</span></span>
<span data-ttu-id="ef1b2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef1b2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef1b2-119">-InputObject</span></span>
<span data-ttu-id="ef1b2-120">ServiceBus-Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef1b2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ef1b2-121">-Namespace</span></span>
<span data-ttu-id="ef1b2-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-122">Namespace Name.</span></span>

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

### <span data-ttu-id="ef1b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef1b2-124">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ef1b2-124">The name of the resource group</span></span>

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

### <span data-ttu-id="ef1b2-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="ef1b2-125">-Topic</span></span>
<span data-ttu-id="ef1b2-126">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-126">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef1b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1b2-127">CommonParameters</span></span>
<span data-ttu-id="ef1b2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef1b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1b2-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1b2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef1b2-130">INPUTS</span></span>

### <span data-ttu-id="ef1b2-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef1b2-131">-ResourceGroup</span></span>
 <span data-ttu-id="ef1b2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1b2-132">System.String</span></span>

### <span data-ttu-id="ef1b2-133">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="ef1b2-133">-NamespaceName</span></span>
 <span data-ttu-id="ef1b2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1b2-134">System.String</span></span>

### <span data-ttu-id="ef1b2-135">-Topicname</span><span class="sxs-lookup"><span data-stu-id="ef1b2-135">-TopicName</span></span>
 <span data-ttu-id="ef1b2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1b2-136">System.String</span></span>

### <span data-ttu-id="ef1b2-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="ef1b2-137">-SubscriptionObj</span></span>
 <span data-ttu-id="ef1b2-138">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ef1b2-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="ef1b2-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef1b2-139">OUTPUTS</span></span>

### <span data-ttu-id="ef1b2-140">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ef1b2-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="ef1b2-141">Name: SB-TopicSubscription-beispiel1 Ort: West US AccessedAt: 1/1/0001 12:00:00 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 pm DefaultMessageTimeToLive: 10675199.02:05.4775807: DeadLetteringOnFilterEvaluationExceptions DeadLetteringOnMessageExpiration: EnableBatchedOperations: EntityAvailabilityStatus: Lock Duration: MaxDeliveryCount: MessageCount:. RequiresSession: 1/20/2017 9:59:15 00:01:00 UpdatedAt::::</span><span class="sxs-lookup"><span data-stu-id="ef1b2-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="ef1b2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef1b2-142">NOTES</span></span>

## <span data-ttu-id="ef1b2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef1b2-143">RELATED LINKS</span></span>

