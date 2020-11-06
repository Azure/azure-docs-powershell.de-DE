---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478950"
---
# <span data-ttu-id="86a1b-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="86a1b-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="86a1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="86a1b-103">Gibt eine Beschreibung des Abonnements für das angegebene Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="86a1b-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86a1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86a1b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="86a1b-106">Das Cmdlet " **Get-AzureRmServiceBusSubscription** " gibt eine Beschreibung des Abonnements für das angegebene ServiceBus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="86a1b-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="86a1b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="86a1b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86a1b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="86a1b-109">Gibt eine Beschreibung des Abonnements für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="86a1b-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="86a1b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86a1b-110">PARAMETERS</span></span>

### <span data-ttu-id="86a1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a1b-111">-DefaultProfile</span></span>
<span data-ttu-id="86a1b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86a1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86a1b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="86a1b-113">-Name</span></span>
<span data-ttu-id="86a1b-114">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="86a1b-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a1b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86a1b-115">-Namespace</span></span>
<span data-ttu-id="86a1b-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="86a1b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="86a1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="86a1b-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="86a1b-118">The name of the resource group</span></span>

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

### <span data-ttu-id="86a1b-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="86a1b-119">-Topic</span></span>
<span data-ttu-id="86a1b-120">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="86a1b-120">Topic Name.</span></span>

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

### <span data-ttu-id="86a1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a1b-121">CommonParameters</span></span>
<span data-ttu-id="86a1b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a1b-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a1b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a1b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86a1b-124">INPUTS</span></span>

### <span data-ttu-id="86a1b-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86a1b-125">-ResourceGroup</span></span>
 <span data-ttu-id="86a1b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="86a1b-126">System.String</span></span>
 

### <span data-ttu-id="86a1b-127">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="86a1b-127">-NamespaceName</span></span>
 <span data-ttu-id="86a1b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="86a1b-128">System.String</span></span>
 

### <span data-ttu-id="86a1b-129">-Topicname</span><span class="sxs-lookup"><span data-stu-id="86a1b-129">-TopicName</span></span>
 <span data-ttu-id="86a1b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="86a1b-130">System.String</span></span>
 

### <span data-ttu-id="86a1b-131">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="86a1b-131">-SubscriptionName</span></span>
 <span data-ttu-id="86a1b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="86a1b-132">System.String</span></span>
 

## <span data-ttu-id="86a1b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86a1b-133">OUTPUTS</span></span>

### <span data-ttu-id="86a1b-134">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="86a1b-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="86a1b-135">Name: SB-TopicSubscription-beispiel1 Ort: West-US-AccessedAt: 1/20/2017 3:18:54 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 am DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: available IsReadOnly: Lock Duration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: Falscher Status: Active UpdatedAt: 1/20/2017 3:18:54 am</span><span class="sxs-lookup"><span data-stu-id="86a1b-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="86a1b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="86a1b-136">NOTES</span></span>

## <span data-ttu-id="86a1b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86a1b-137">RELATED LINKS</span></span>

