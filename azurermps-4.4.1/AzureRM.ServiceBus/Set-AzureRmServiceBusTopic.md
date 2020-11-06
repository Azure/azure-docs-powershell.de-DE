---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 4b346d1ef4757d74ac9c663f5c72a134d5c48153
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496849"
---
# <span data-ttu-id="ccfa8-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ccfa8-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="ccfa8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccfa8-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfa8-103">Aktualisiert die Beschreibung eines Service Bus-Themas im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccfa8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccfa8-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccfa8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccfa8-105">DESCRIPTION</span></span>
<span data-ttu-id="ccfa8-106">Das Cmdlet " **Satz-AzureRmServiceBusTopic** " aktualisiert ein Beschreibungsobjekt für ein Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ccfa8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccfa8-107">EXAMPLES</span></span>

### <span data-ttu-id="ccfa8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ccfa8-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj
```

<span data-ttu-id="ccfa8-109">Aktualisiert das angegebene Thema mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="ccfa8-110">In diesem Beispiel wird die **EnableExpress** -Eigenschaft auf **true** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="ccfa8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccfa8-111">PARAMETERS</span></span>

### <span data-ttu-id="ccfa8-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ccfa8-112">-Confirm</span></span>
<span data-ttu-id="ccfa8-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccfa8-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccfa8-114">-WhatIf</span></span>
<span data-ttu-id="ccfa8-115">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccfa8-116">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccfa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccfa8-117">-DefaultProfile</span></span>
<span data-ttu-id="ccfa8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccfa8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ccfa8-119">-InputObject</span></span>
<span data-ttu-id="ccfa8-120">ServiceBus-Themen Definition</span><span class="sxs-lookup"><span data-stu-id="ccfa8-120">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccfa8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ccfa8-121">-Name</span></span>
<span data-ttu-id="ccfa8-122">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-122">Topic Name.</span></span>

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

### <span data-ttu-id="ccfa8-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ccfa8-123">-Namespace</span></span>
<span data-ttu-id="ccfa8-124">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-124">Namespace Name.</span></span>

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

### <span data-ttu-id="ccfa8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccfa8-125">-ResourceGroupName</span></span>
<span data-ttu-id="ccfa8-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ccfa8-126">The name of the resource group</span></span>

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

### <span data-ttu-id="ccfa8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfa8-127">CommonParameters</span></span>
<span data-ttu-id="ccfa8-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccfa8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfa8-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccfa8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfa8-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccfa8-130">INPUTS</span></span>

### <span data-ttu-id="ccfa8-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ccfa8-131">-ResourceGroup</span></span>
 <span data-ttu-id="ccfa8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ccfa8-132">System.String</span></span>

### <span data-ttu-id="ccfa8-133">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="ccfa8-133">-NamespaceName</span></span>
 <span data-ttu-id="ccfa8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ccfa8-134">System.String</span></span>

### <span data-ttu-id="ccfa8-135">-Topicname</span><span class="sxs-lookup"><span data-stu-id="ccfa8-135">-TopicName</span></span>
 <span data-ttu-id="ccfa8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ccfa8-136">System.String</span></span>

### <span data-ttu-id="ccfa8-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="ccfa8-137">-TopicObj</span></span>
 <span data-ttu-id="ccfa8-138">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ccfa8-138">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>

## <span data-ttu-id="ccfa8-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccfa8-139">OUTPUTS</span></span>

### <span data-ttu-id="ccfa8-140">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ccfa8-140">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="ccfa8-141">Name: SB-Topic_exampl1 Ort: West US ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/topics/SB-Topic_exampl1 geben Sie Folgendes ein: Microsoft. ServiceBus/Topic AccessedAt: 1/20/2017 3:18:54 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 am CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: true EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false ISEXpress: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false sizeInBytes: 0-Status: SubscriptionCount: SupportOrdering: UpdatedAt: falsch: 1/20/2017 7:12:16 Uhr</span><span class="sxs-lookup"><span data-stu-id="ccfa8-141">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB- Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : True EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 7:12:16 PM</span></span>

## <span data-ttu-id="ccfa8-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccfa8-142">NOTES</span></span>

## <span data-ttu-id="ccfa8-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccfa8-143">RELATED LINKS</span></span>

