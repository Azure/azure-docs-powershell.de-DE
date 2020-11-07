---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 6bb5b6e8ea96f0852747c00ac4ef5ac11208e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662561"
---
# <span data-ttu-id="2106f-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="2106f-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="2106f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2106f-102">SYNOPSIS</span></span>
<span data-ttu-id="2106f-103">Aktualisiert eine Abonnementbeschreibung für ein Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2106f-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2106f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2106f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2106f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2106f-105">DESCRIPTION</span></span>
<span data-ttu-id="2106f-106">Das Cmdlet " **Satz-AzureRmServiceBusSubscription** " aktualisiert die Beschreibung des Abonnements für das ServiceBus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2106f-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2106f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2106f-107">EXAMPLES</span></span>

### <span data-ttu-id="2106f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2106f-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="2106f-109">Aktualisiert die Beschreibung des angegebenen Abonnements für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="2106f-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="2106f-110">In diesem Beispiel wird die **DeadLetteringOnMessageExpiration** -Eigenschaft auf **true** und **MaxDeliveryCount** auf 9 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2106f-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="2106f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2106f-111">PARAMETERS</span></span>

### <span data-ttu-id="2106f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2106f-112">-DefaultProfile</span></span>
<span data-ttu-id="2106f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2106f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2106f-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2106f-114">-InputObject</span></span>
<span data-ttu-id="2106f-115">ServiceBus-Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="2106f-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2106f-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2106f-116">-Namespace</span></span>
<span data-ttu-id="2106f-117">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="2106f-117">Namespace Name.</span></span>

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

### <span data-ttu-id="2106f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2106f-118">-ResourceGroupName</span></span>
<span data-ttu-id="2106f-119">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2106f-119">The name of the resource group</span></span>

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

### <span data-ttu-id="2106f-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="2106f-120">-Topic</span></span>
<span data-ttu-id="2106f-121">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="2106f-121">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2106f-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2106f-122">-Confirm</span></span>
<span data-ttu-id="2106f-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2106f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2106f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2106f-124">-WhatIf</span></span>
<span data-ttu-id="2106f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2106f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2106f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2106f-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2106f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2106f-127">CommonParameters</span></span>
<span data-ttu-id="2106f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2106f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2106f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2106f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2106f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2106f-130">INPUTS</span></span>

### <span data-ttu-id="2106f-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2106f-131">-ResourceGroup</span></span>
 <span data-ttu-id="2106f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2106f-132">System.String</span></span>

### <span data-ttu-id="2106f-133">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="2106f-133">-NamespaceName</span></span>
 <span data-ttu-id="2106f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2106f-134">System.String</span></span>

### <span data-ttu-id="2106f-135">-Topicname</span><span class="sxs-lookup"><span data-stu-id="2106f-135">-TopicName</span></span>
 <span data-ttu-id="2106f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2106f-136">System.String</span></span>

### <span data-ttu-id="2106f-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="2106f-137">-SubscriptionObj</span></span>
 <span data-ttu-id="2106f-138">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="2106f-138">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="2106f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2106f-139">OUTPUTS</span></span>

### <span data-ttu-id="2106f-140">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="2106f-140">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="2106f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2106f-141">NOTES</span></span>

## <span data-ttu-id="2106f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2106f-142">RELATED LINKS</span></span>

