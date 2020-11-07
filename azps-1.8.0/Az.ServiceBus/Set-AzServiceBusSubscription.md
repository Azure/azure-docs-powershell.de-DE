---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: d05a8bb98910a478790581b21a0f4ee7be710ea1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659342"
---
# <span data-ttu-id="bd776-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bd776-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="bd776-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd776-102">SYNOPSIS</span></span>
<span data-ttu-id="bd776-103">Aktualisiert eine Abonnementbeschreibung für ein Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="bd776-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bd776-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd776-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd776-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd776-105">DESCRIPTION</span></span>
<span data-ttu-id="bd776-106">Das Cmdlet " **Satz-AzServiceBusSubscription** " aktualisiert die Beschreibung des Abonnements für das ServiceBus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="bd776-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bd776-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd776-107">EXAMPLES</span></span>

### <span data-ttu-id="bd776-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd776-108">Example 1</span></span>
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

<span data-ttu-id="bd776-109">Aktualisiert die Beschreibung des angegebenen Abonnements für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="bd776-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="bd776-110">In diesem Beispiel wird die **DeadLetteringOnMessageExpiration** -Eigenschaft auf **true** und **MaxDeliveryCount** auf 9 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bd776-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="bd776-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd776-111">PARAMETERS</span></span>

### <span data-ttu-id="bd776-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd776-112">-DefaultProfile</span></span>
<span data-ttu-id="bd776-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd776-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd776-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd776-114">-InputObject</span></span>
<span data-ttu-id="bd776-115">ServiceBus-Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="bd776-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="bd776-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd776-116">-Namespace</span></span>
<span data-ttu-id="bd776-117">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="bd776-117">Namespace Name.</span></span>

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

### <span data-ttu-id="bd776-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd776-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd776-119">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bd776-119">The name of the resource group</span></span>

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

### <span data-ttu-id="bd776-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="bd776-120">-Topic</span></span>
<span data-ttu-id="bd776-121">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="bd776-121">Topic Name.</span></span>

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

### <span data-ttu-id="bd776-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd776-122">-Confirm</span></span>
<span data-ttu-id="bd776-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd776-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd776-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd776-124">-WhatIf</span></span>
<span data-ttu-id="bd776-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd776-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd776-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd776-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd776-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd776-127">CommonParameters</span></span>
<span data-ttu-id="bd776-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd776-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd776-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd776-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd776-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd776-130">INPUTS</span></span>

### <span data-ttu-id="bd776-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bd776-131">System.String</span></span>

### <span data-ttu-id="bd776-132">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bd776-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bd776-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd776-133">OUTPUTS</span></span>

### <span data-ttu-id="bd776-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bd776-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bd776-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd776-135">NOTES</span></span>

## <span data-ttu-id="bd776-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd776-136">RELATED LINKS</span></span>
