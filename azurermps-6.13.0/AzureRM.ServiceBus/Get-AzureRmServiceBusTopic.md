---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: ddccdb907dac89466a81be62e104202a3e59a672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501065"
---
# <span data-ttu-id="1fb6a-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1fb6a-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="1fb6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb6a-103">Gibt eine Beschreibung für das angegebene Service Bus-Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fb6a-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb6a-106">Das Cmdlet " **Get-AzureRmServiceBusTopic** " gibt eine Themenbeschreibung für den angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1fb6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="1fb6a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fb6a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="1fb6a-109">Gibt die Beschreibung des angegebenen Themas für den angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="1fb6a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1fb6a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="1fb6a-111">Gibt eine Liste der Themen für den angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="1fb6a-112">Standardmäßig werden 100-Themen zurückgegeben, wenn mehr als 100 Themen zurückgegeben werden sollen, verwenden Sie bitte-MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="1fb6a-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1fb6a-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="1fb6a-114">Gibt eine Liste der ersten 150-Themen für den angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="1fb6a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fb6a-115">PARAMETERS</span></span>

### <span data-ttu-id="1fb6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb6a-116">-DefaultProfile</span></span>
<span data-ttu-id="1fb6a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb6a-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1fb6a-118">-MaxCount</span></span>
<span data-ttu-id="1fb6a-119">Ermitteln Sie die maximale Anzahl von Themen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="1fb6a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1fb6a-120">-Name</span></span>
<span data-ttu-id="1fb6a-121">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="1fb6a-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb6a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1fb6a-122">-Namespace</span></span>
<span data-ttu-id="1fb6a-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="1fb6a-123">Namespace Name</span></span>

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

### <span data-ttu-id="1fb6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fb6a-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1fb6a-125">The name of the resource group</span></span>

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

### <span data-ttu-id="1fb6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb6a-126">CommonParameters</span></span>
<span data-ttu-id="1fb6a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb6a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb6a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fb6a-129">INPUTS</span></span>

### <span data-ttu-id="1fb6a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb6a-130">System.String</span></span>

## <span data-ttu-id="1fb6a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fb6a-131">OUTPUTS</span></span>

### <span data-ttu-id="1fb6a-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="1fb6a-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1fb6a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fb6a-133">NOTES</span></span>

## <span data-ttu-id="1fb6a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fb6a-134">RELATED LINKS</span></span>
