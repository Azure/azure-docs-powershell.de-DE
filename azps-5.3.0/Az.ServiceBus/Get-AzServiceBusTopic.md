---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471909"
---
# <span data-ttu-id="e267e-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e267e-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="e267e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e267e-102">SYNOPSIS</span></span>
<span data-ttu-id="e267e-103">Gibt eine Beschreibung für das angegebene Thema "Dienstbus" zurück.</span><span class="sxs-lookup"><span data-stu-id="e267e-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="e267e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e267e-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e267e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e267e-105">DESCRIPTION</span></span>
<span data-ttu-id="e267e-106">Das **Cmdlet "Get-AzServiceBusTopic"** gibt eine Themenbeschreibung für den angegebenen Namespace "Service Bus" zurück.</span><span class="sxs-lookup"><span data-stu-id="e267e-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e267e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e267e-107">EXAMPLES</span></span>

### <span data-ttu-id="e267e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e267e-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

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

<span data-ttu-id="e267e-109">Gibt die Beschreibung des angegebenen Themas für den angegebenen Namespace "Service Bus" zurück.</span><span class="sxs-lookup"><span data-stu-id="e267e-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="e267e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e267e-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="e267e-111">Gibt eine Liste der Themen für den angegebenen Namespace "Service Bus" zurück.</span><span class="sxs-lookup"><span data-stu-id="e267e-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="e267e-112">Standardmäßig werden 100 Themen zurückgegeben, wenn mehr als 100 Themen zurückgegeben werden sollen, verwenden Sie den Parameter "-MaxCount".</span><span class="sxs-lookup"><span data-stu-id="e267e-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="e267e-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e267e-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="e267e-114">Gibt eine Liste der ersten 150 Themen für den angegebenen Namespace "Service Bus" zurück.</span><span class="sxs-lookup"><span data-stu-id="e267e-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="e267e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e267e-115">PARAMETERS</span></span>

### <span data-ttu-id="e267e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e267e-116">-DefaultProfile</span></span>
<span data-ttu-id="e267e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e267e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e267e-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e267e-118">-MaxCount</span></span>
<span data-ttu-id="e267e-119">Ermitteln Sie die maximale Anzahl von Themen, die sie zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="e267e-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="e267e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e267e-120">-Name</span></span>
<span data-ttu-id="e267e-121">Themaname</span><span class="sxs-lookup"><span data-stu-id="e267e-121">Topic Name</span></span>

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

### <span data-ttu-id="e267e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e267e-122">-Namespace</span></span>
<span data-ttu-id="e267e-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="e267e-123">Namespace Name</span></span>

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

### <span data-ttu-id="e267e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e267e-124">-ResourceGroupName</span></span>
<span data-ttu-id="e267e-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e267e-125">The name of the resource group</span></span>

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

### <span data-ttu-id="e267e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e267e-126">CommonParameters</span></span>
<span data-ttu-id="e267e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e267e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e267e-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e267e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e267e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e267e-129">INPUTS</span></span>

### <span data-ttu-id="e267e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e267e-130">System.String</span></span>

## <span data-ttu-id="e267e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e267e-131">OUTPUTS</span></span>

### <span data-ttu-id="e267e-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="e267e-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e267e-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e267e-133">NOTES</span></span>

## <span data-ttu-id="e267e-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e267e-134">RELATED LINKS</span></span>
