---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482722"
---
# <span data-ttu-id="80e99-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="80e99-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="80e99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80e99-102">SYNOPSIS</span></span>
<span data-ttu-id="80e99-103">Aktualisiert die Beschreibung einer Service Bus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="80e99-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80e99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80e99-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80e99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80e99-105">DESCRIPTION</span></span>
<span data-ttu-id="80e99-106">Das Cmdlet " **Satz-AzureRmServiceBusQueue** " aktualisiert die Beschreibung für die ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="80e99-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="80e99-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80e99-107">EXAMPLES</span></span>

### <span data-ttu-id="80e99-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80e99-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="80e99-109">Aktualisiert die angegebene Warteschlange mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="80e99-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="80e99-110">In diesem Beispiel wird die **DeadLetteringOnMessageExpiration** -Eigenschaft auf **true** und **SupportOrdering** auf **true** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80e99-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="80e99-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="80e99-111">PARAMETERS</span></span>

### <span data-ttu-id="80e99-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e99-112">-DefaultProfile</span></span>
<span data-ttu-id="80e99-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80e99-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80e99-114">-InputObject</span></span>
<span data-ttu-id="80e99-115">ServiceBus-Definition.</span><span class="sxs-lookup"><span data-stu-id="80e99-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-116">-Name</span><span class="sxs-lookup"><span data-stu-id="80e99-116">-Name</span></span>
<span data-ttu-id="80e99-117">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="80e99-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80e99-118">-Namespace</span></span>
<span data-ttu-id="80e99-119">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="80e99-119">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e99-120">-ResourceGroupName</span></span>
<span data-ttu-id="80e99-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="80e99-121">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80e99-122">-Confirm</span></span>
<span data-ttu-id="80e99-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80e99-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e99-124">-WhatIf</span></span>
<span data-ttu-id="80e99-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80e99-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80e99-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80e99-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e99-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e99-127">CommonParameters</span></span>
<span data-ttu-id="80e99-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e99-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e99-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e99-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e99-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80e99-130">INPUTS</span></span>

### <span data-ttu-id="80e99-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="80e99-131">-ResourceGroup</span></span>
 <span data-ttu-id="80e99-132">System. String</span><span class="sxs-lookup"><span data-stu-id="80e99-132">System.String</span></span>

### <span data-ttu-id="80e99-133">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="80e99-133">-NamespaceName</span></span>
 <span data-ttu-id="80e99-134">System. String</span><span class="sxs-lookup"><span data-stu-id="80e99-134">System.String</span></span>

### <span data-ttu-id="80e99-135">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="80e99-135">-QueueName</span></span>
 <span data-ttu-id="80e99-136">System. String</span><span class="sxs-lookup"><span data-stu-id="80e99-136">System.String</span></span>

### <span data-ttu-id="80e99-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="80e99-137">-QueueObj</span></span>
 <span data-ttu-id="80e99-138">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="80e99-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="80e99-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80e99-139">OUTPUTS</span></span>

### <span data-ttu-id="80e99-140">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="80e99-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="80e99-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="80e99-141">NOTES</span></span>

## <span data-ttu-id="80e99-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80e99-142">RELATED LINKS</span></span>

