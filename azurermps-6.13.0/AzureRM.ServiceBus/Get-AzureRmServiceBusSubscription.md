---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 03d85b0b31261330f6245e7439847df04d68d56b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499406"
---
# <span data-ttu-id="30aee-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="30aee-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="30aee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30aee-102">SYNOPSIS</span></span>
<span data-ttu-id="30aee-103">Gibt eine Beschreibung des Abonnements für das angegebene Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="30aee-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30aee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30aee-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30aee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30aee-105">DESCRIPTION</span></span>
<span data-ttu-id="30aee-106">Das Cmdlet " **Get-AzureRmServiceBusSubscription** " gibt eine Beschreibung des Abonnements für das angegebene ServiceBus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="30aee-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="30aee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30aee-107">EXAMPLES</span></span>

### <span data-ttu-id="30aee-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30aee-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="30aee-109">Gibt eine Beschreibung des Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="30aee-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="30aee-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="30aee-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="30aee-111">Gibt die Liste der Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="30aee-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="30aee-112">Standardmäßig werden 100-Abonnements zurückgegeben, für die Anzahl der Abonnements verwenden Sie bitte-MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="30aee-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="30aee-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="30aee-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="30aee-114">Gibt die Liste der ersten 150-Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="30aee-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="30aee-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="30aee-115">PARAMETERS</span></span>

### <span data-ttu-id="30aee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30aee-116">-DefaultProfile</span></span>
<span data-ttu-id="30aee-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30aee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30aee-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="30aee-118">-MaxCount</span></span>
<span data-ttu-id="30aee-119">Ermitteln Sie die maximale Anzahl von Abonnements, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30aee-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="30aee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="30aee-120">-Name</span></span>
<span data-ttu-id="30aee-121">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="30aee-121">Subscription Name</span></span>

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

### <span data-ttu-id="30aee-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="30aee-122">-Namespace</span></span>
<span data-ttu-id="30aee-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="30aee-123">Namespace Name</span></span>

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

### <span data-ttu-id="30aee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30aee-124">-ResourceGroupName</span></span>
<span data-ttu-id="30aee-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="30aee-125">The name of the resource group</span></span>

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

### <span data-ttu-id="30aee-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="30aee-126">-Topic</span></span>
<span data-ttu-id="30aee-127">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="30aee-127">Topic Name</span></span>

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

### <span data-ttu-id="30aee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30aee-128">CommonParameters</span></span>
<span data-ttu-id="30aee-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30aee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30aee-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30aee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30aee-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30aee-131">INPUTS</span></span>

### <span data-ttu-id="30aee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="30aee-132">System.String</span></span>

## <span data-ttu-id="30aee-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30aee-133">OUTPUTS</span></span>

### <span data-ttu-id="30aee-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="30aee-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="30aee-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="30aee-135">NOTES</span></span>

## <span data-ttu-id="30aee-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30aee-136">RELATED LINKS</span></span>
