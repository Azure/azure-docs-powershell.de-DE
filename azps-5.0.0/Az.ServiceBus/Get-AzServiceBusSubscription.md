---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175892"
---
# <span data-ttu-id="4e4db-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4e4db-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="4e4db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e4db-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4db-103">Gibt eine Beschreibung des Abonnements für das angegebene Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4db-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="4e4db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e4db-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e4db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e4db-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4db-106">Das Cmdlet " **Get-AzServiceBusSubscription** " gibt eine Beschreibung des Abonnements für das angegebene ServiceBus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4db-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="4e4db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e4db-107">EXAMPLES</span></span>

### <span data-ttu-id="4e4db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e4db-108">Example 1</span></span>
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

<span data-ttu-id="4e4db-109">Gibt eine Beschreibung des Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4db-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="4e4db-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4e4db-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="4e4db-111">Gibt die Liste der Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4db-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="4e4db-112">Standardmäßig werden 100-Abonnements zurückgegeben, für die Anzahl der Abonnements verwenden Sie bitte-MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="4e4db-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="4e4db-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4e4db-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="4e4db-114">Gibt die Liste der ersten 150-Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4db-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="4e4db-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e4db-115">PARAMETERS</span></span>

### <span data-ttu-id="4e4db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4db-116">-DefaultProfile</span></span>
<span data-ttu-id="4e4db-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e4db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4db-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4e4db-118">-MaxCount</span></span>
<span data-ttu-id="4e4db-119">Ermitteln Sie die maximale Anzahl von Abonnements, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e4db-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="4e4db-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4e4db-120">-Name</span></span>
<span data-ttu-id="4e4db-121">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="4e4db-121">Subscription Name</span></span>

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

### <span data-ttu-id="4e4db-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e4db-122">-Namespace</span></span>
<span data-ttu-id="4e4db-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4e4db-123">Namespace Name</span></span>

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

### <span data-ttu-id="4e4db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e4db-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e4db-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4e4db-125">The name of the resource group</span></span>

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

### <span data-ttu-id="4e4db-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="4e4db-126">-Topic</span></span>
<span data-ttu-id="4e4db-127">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="4e4db-127">Topic Name</span></span>

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

### <span data-ttu-id="4e4db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4db-128">CommonParameters</span></span>
<span data-ttu-id="4e4db-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4db-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4db-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4db-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e4db-131">INPUTS</span></span>

### <span data-ttu-id="4e4db-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4e4db-132">System.String</span></span>

## <span data-ttu-id="4e4db-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e4db-133">OUTPUTS</span></span>

### <span data-ttu-id="4e4db-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4e4db-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="4e4db-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e4db-135">NOTES</span></span>

## <span data-ttu-id="4e4db-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e4db-136">RELATED LINKS</span></span>
