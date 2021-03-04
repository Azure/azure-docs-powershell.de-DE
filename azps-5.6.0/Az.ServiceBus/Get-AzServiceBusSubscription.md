---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: c68764d0dfd2d496d5ead3a2e9631d29979194e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939944"
---
# <span data-ttu-id="b29cf-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="b29cf-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="b29cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b29cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b29cf-103">Gibt eine Abonnementbeschreibung für das angegebene Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="b29cf-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="b29cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b29cf-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b29cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b29cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b29cf-106">Das **Get-AzServiceBusSubscription-Cmdlet** gibt eine Abonnementbeschreibung für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="b29cf-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="b29cf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b29cf-107">EXAMPLES</span></span>

### <span data-ttu-id="b29cf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b29cf-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="b29cf-109">Gibt eine Abonnementbeschreibung für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="b29cf-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="b29cf-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b29cf-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="b29cf-111">Gibt eine Liste der Abonnements für das angegebene Thema "Dienstbus" zurück.</span><span class="sxs-lookup"><span data-stu-id="b29cf-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="b29cf-112">Standardmäßig werden 100 Abonnements zurückgegeben, für die Anzahl der Abonnements verwenden Sie bitte -MaxCount Parameter.</span><span class="sxs-lookup"><span data-stu-id="b29cf-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="b29cf-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b29cf-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="b29cf-114">Gibt eine Liste der ersten 150 Abonnements für das angegebene Thema "Dienstbus" zurück.</span><span class="sxs-lookup"><span data-stu-id="b29cf-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="b29cf-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b29cf-115">PARAMETERS</span></span>

### <span data-ttu-id="b29cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29cf-116">-DefaultProfile</span></span>
<span data-ttu-id="b29cf-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b29cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b29cf-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b29cf-118">-MaxCount</span></span>
<span data-ttu-id="b29cf-119">Ermitteln Sie die maximale Anzahl von Abonnements, die sie zurückgeben soll.</span><span class="sxs-lookup"><span data-stu-id="b29cf-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="b29cf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b29cf-120">-Name</span></span>
<span data-ttu-id="b29cf-121">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="b29cf-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29cf-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b29cf-122">-Namespace</span></span>
<span data-ttu-id="b29cf-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="b29cf-123">Namespace Name</span></span>

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

### <span data-ttu-id="b29cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="b29cf-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b29cf-125">The name of the resource group</span></span>

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

### <span data-ttu-id="b29cf-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="b29cf-126">-Topic</span></span>
<span data-ttu-id="b29cf-127">Topic Name</span><span class="sxs-lookup"><span data-stu-id="b29cf-127">Topic Name</span></span>

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

### <span data-ttu-id="b29cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29cf-128">CommonParameters</span></span>
<span data-ttu-id="b29cf-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29cf-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29cf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29cf-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b29cf-131">INPUTS</span></span>

### <span data-ttu-id="b29cf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b29cf-132">System.String</span></span>

## <span data-ttu-id="b29cf-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b29cf-133">OUTPUTS</span></span>

### <span data-ttu-id="b29cf-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="b29cf-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="b29cf-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b29cf-135">NOTES</span></span>

## <span data-ttu-id="b29cf-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b29cf-136">RELATED LINKS</span></span>
