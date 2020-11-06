---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478942"
---
# <span data-ttu-id="f8fa9-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f8fa9-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="f8fa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fa9-103">Gibt eine Beschreibung für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8fa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8fa9-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8fa9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="f8fa9-106">Das Cmdlet " **Get-AzureRmServiceBusTopic** " gibt eine Themenbeschreibung für den angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f8fa9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="f8fa9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8fa9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="f8fa9-109">Gibt die Beschreibung des angegebenen Themas für den angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="f8fa9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="f8fa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fa9-111">-DefaultProfile</span></span>
<span data-ttu-id="f8fa9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8fa9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f8fa9-113">-Name</span></span>
<span data-ttu-id="f8fa9-114">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8fa9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8fa9-115">-Namespace</span></span>
<span data-ttu-id="f8fa9-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-116">Namespace Name.</span></span>

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

### <span data-ttu-id="f8fa9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fa9-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8fa9-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f8fa9-118">The name of the resource group</span></span>

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

### <span data-ttu-id="f8fa9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fa9-119">CommonParameters</span></span>
<span data-ttu-id="f8fa9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fa9-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8fa9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fa9-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8fa9-122">INPUTS</span></span>

### <span data-ttu-id="f8fa9-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8fa9-123">-ResourceGroup</span></span>
 <span data-ttu-id="f8fa9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f8fa9-124">System.String</span></span>
 

### <span data-ttu-id="f8fa9-125">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="f8fa9-125">-NamespaceName</span></span>
 <span data-ttu-id="f8fa9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8fa9-126">System.String</span></span>
 

### <span data-ttu-id="f8fa9-127">-Topicname</span><span class="sxs-lookup"><span data-stu-id="f8fa9-127">-TopicName</span></span>
 <span data-ttu-id="f8fa9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f8fa9-128">System.String</span></span>

## <span data-ttu-id="f8fa9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8fa9-129">OUTPUTS</span></span>

### <span data-ttu-id="f8fa9-130">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="f8fa9-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="f8fa9-131">Name: SB-Topic_exampl1 Ort: West US ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/topics/S B-Topic_exampl1 Typ: Microsoft. ServiceBus/Topic AccessedAt: 1/20/2017 3:18:54 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 am CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false ISEXpress: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false sizeInBytes: 0 Status: SubscriptionCount: SupportOrdering: falsch UpdatedAt: 1/20/2017 3:16:43 am</span><span class="sxs-lookup"><span data-stu-id="f8fa9-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="f8fa9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8fa9-132">NOTES</span></span>

## <span data-ttu-id="f8fa9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8fa9-133">RELATED LINKS</span></span>

