---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 67ce9249134365aa182024dff6e5913f68e11738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659341"
---
# <span data-ttu-id="39b4b-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="39b4b-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="39b4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="39b4b-103">Aktualisiert die Beschreibung eines Service Bus-Themas im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="39b4b-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="39b4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39b4b-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39b4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="39b4b-106">Das Cmdlet " **Satz-AzServiceBusTopic** " aktualisiert ein Beschreibungsobjekt für ein Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="39b4b-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="39b4b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="39b4b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39b4b-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="39b4b-109">Aktualisiert das angegebene Thema mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="39b4b-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="39b4b-110">In diesem Beispiel wird die **EnableExpress** -Eigenschaft auf **true** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="39b4b-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="39b4b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39b4b-111">PARAMETERS</span></span>

### <span data-ttu-id="39b4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b4b-112">-DefaultProfile</span></span>
<span data-ttu-id="39b4b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39b4b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39b4b-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39b4b-114">-InputObject</span></span>
<span data-ttu-id="39b4b-115">ServiceBus-Themen Definition</span><span class="sxs-lookup"><span data-stu-id="39b4b-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39b4b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="39b4b-116">-Name</span></span>
<span data-ttu-id="39b4b-117">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="39b4b-117">Topic Name.</span></span>

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

### <span data-ttu-id="39b4b-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="39b4b-118">-Namespace</span></span>
<span data-ttu-id="39b4b-119">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="39b4b-119">Namespace Name.</span></span>

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

### <span data-ttu-id="39b4b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b4b-120">-ResourceGroupName</span></span>
<span data-ttu-id="39b4b-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="39b4b-121">The name of the resource group</span></span>

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

### <span data-ttu-id="39b4b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39b4b-122">-Confirm</span></span>
<span data-ttu-id="39b4b-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39b4b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b4b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b4b-124">-WhatIf</span></span>
<span data-ttu-id="39b4b-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39b4b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39b4b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39b4b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b4b-127">CommonParameters</span></span>
<span data-ttu-id="39b4b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b4b-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b4b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b4b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39b4b-130">INPUTS</span></span>

### <span data-ttu-id="39b4b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="39b4b-131">System.String</span></span>

### <span data-ttu-id="39b4b-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="39b4b-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="39b4b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39b4b-133">OUTPUTS</span></span>

### <span data-ttu-id="39b4b-134">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="39b4b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="39b4b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="39b4b-135">NOTES</span></span>

## <span data-ttu-id="39b4b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39b4b-136">RELATED LINKS</span></span>
