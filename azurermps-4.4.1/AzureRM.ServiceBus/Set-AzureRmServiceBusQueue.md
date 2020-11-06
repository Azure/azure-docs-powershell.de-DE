---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: cd291e6c33dd08668c7a78f2c739f65c576e2f0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503942"
---
# <span data-ttu-id="0b54c-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0b54c-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="0b54c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b54c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b54c-103">Aktualisiert die Beschreibung einer Service Bus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0b54c-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b54c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b54c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b54c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b54c-105">DESCRIPTION</span></span>
<span data-ttu-id="0b54c-106">Das Cmdlet " **Satz-AzureRmServiceBusQueue** " aktualisiert die Beschreibung für die ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0b54c-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0b54c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b54c-107">EXAMPLES</span></span>

### <span data-ttu-id="0b54c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b54c-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj
```

<span data-ttu-id="0b54c-109">Aktualisiert die angegebene Warteschlange mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="0b54c-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="0b54c-110">In diesem Beispiel wird die **DeadLetteringOnMessageExpiration** -Eigenschaft auf **true** und **SupportOrdering** auf **true** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0b54c-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="0b54c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b54c-111">PARAMETERS</span></span>

### <span data-ttu-id="0b54c-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b54c-112">-Confirm</span></span>
<span data-ttu-id="0b54c-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b54c-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b54c-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b54c-114">-WhatIf</span></span>
<span data-ttu-id="0b54c-115">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b54c-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b54c-116">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b54c-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b54c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b54c-117">-DefaultProfile</span></span>
<span data-ttu-id="0b54c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b54c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b54c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b54c-119">-InputObject</span></span>
<span data-ttu-id="0b54c-120">ServiceBus-Definition.</span><span class="sxs-lookup"><span data-stu-id="0b54c-120">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b54c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b54c-121">-Name</span></span>
<span data-ttu-id="0b54c-122">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="0b54c-122">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b54c-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b54c-123">-Namespace</span></span>
<span data-ttu-id="0b54c-124">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="0b54c-124">Namespace Name.</span></span>

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

### <span data-ttu-id="0b54c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b54c-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b54c-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0b54c-126">The name of the resource group</span></span>

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

### <span data-ttu-id="0b54c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b54c-127">CommonParameters</span></span>
<span data-ttu-id="0b54c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b54c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b54c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b54c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b54c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b54c-130">INPUTS</span></span>

### <span data-ttu-id="0b54c-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b54c-131">-ResourceGroup</span></span>
 <span data-ttu-id="0b54c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0b54c-132">System.String</span></span>

### <span data-ttu-id="0b54c-133">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="0b54c-133">-NamespaceName</span></span>
 <span data-ttu-id="0b54c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0b54c-134">System.String</span></span>

### <span data-ttu-id="0b54c-135">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="0b54c-135">-QueueName</span></span>
 <span data-ttu-id="0b54c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0b54c-136">System.String</span></span>

### <span data-ttu-id="0b54c-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="0b54c-137">-QueueObj</span></span>
 <span data-ttu-id="0b54c-138">Microsoft. Azure. Commands. ServiceBus. Models. Queue Attributes</span><span class="sxs-lookup"><span data-stu-id="0b54c-138">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>

## <span data-ttu-id="0b54c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b54c-139">OUTPUTS</span></span>

### <span data-ttu-id="0b54c-140">Microsoft. Azure. Commands. ServiceBus. Models. Queue Attributes</span><span class="sxs-lookup"><span data-stu-id="0b54c-140">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="0b54c-141">Name: SB-Queue_exampl1 Ort: West US Lock Duration: AccessedAt: 1/1/0001 12:00:00 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:34 am DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails RequiresDuplicateDetection: false RequiresSession: false sizeInBytes: Status: Active SupportOrdering: false UpdatedAt: 1/20/2017 6:16:18 pm</span><span class="sxs-lookup"><span data-stu-id="0b54c-141">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:34 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 6:16:18 PM</span></span>

## <span data-ttu-id="0b54c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b54c-142">NOTES</span></span>

## <span data-ttu-id="0b54c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b54c-143">RELATED LINKS</span></span>

