---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368023"
---
# <span data-ttu-id="e2b07-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e2b07-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="e2b07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b07-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b07-103">Erstellt eine Service Buswarteschlange im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e2b07-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e2b07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2b07-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b07-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2b07-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b07-106">Das **Cmdlet "New-AzServiceBusQueue"** erstellt eine Service Bus-Warteschlange im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e2b07-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e2b07-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2b07-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b07-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2b07-108">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="e2b07-109">Erstellt eine neue Service `SB-Queue_example1` Buswarteschlange im angegebenen Namespace des `SB-Example1` Dienstbuss.</span><span class="sxs-lookup"><span data-stu-id="e2b07-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e2b07-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2b07-110">Example 2</span></span>

<span data-ttu-id="e2b07-111">Erstellt eine Service Buswarteschlange im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e2b07-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="e2b07-112">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="e2b07-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="e2b07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2b07-113">PARAMETERS</span></span>

### <span data-ttu-id="e2b07-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="e2b07-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="e2b07-115">Gibt das [TimeSpan-Leerlaufintervall](https://msdn.microsoft.com/library/system.timespan.aspx) an, nach dem die Warteschlange automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e2b07-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="e2b07-116">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e2b07-116">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-117">-DeadOleringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="e2b07-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="e2b07-118">Intschrift bei Nachrichtenablauf</span><span class="sxs-lookup"><span data-stu-id="e2b07-118">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e2b07-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="e2b07-120">Zeitraum bis Zum Livewert.</span><span class="sxs-lookup"><span data-stu-id="e2b07-120">Timespan to live value.</span></span>
<span data-ttu-id="e2b07-121">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Senden der Nachricht an den Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e2b07-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="e2b07-122">Dies ist der Standardwert, der verwendet wird, wenn "TimeToLive" nicht für eine Nachricht selbst festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e2b07-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="e2b07-123">Für Standard = Timespan.Max und Basic = 14 Tage</span><span class="sxs-lookup"><span data-stu-id="e2b07-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b07-124">-DefaultProfile</span></span>
<span data-ttu-id="e2b07-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2b07-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b07-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e2b07-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="e2b07-127">Gibt das Zeitfenster für den doppelten Erkennungsverlauf an. Dies ist ein [TimeSpan-Wert,](https://msdn.microsoft.com/library/system.timespan.aspx) der die Dauer des doppelten Erkennungsverlaufs definiert.</span><span class="sxs-lookup"><span data-stu-id="e2b07-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="e2b07-128">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e2b07-128">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="e2b07-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="e2b07-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span><span class="sxs-lookup"><span data-stu-id="e2b07-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="e2b07-131">-EnableExpress</span></span>
<span data-ttu-id="e2b07-132">EnableExpress – ein Wert, der angibt, ob Expressentitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e2b07-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="e2b07-133">Eine Expresswarteschlange hält eine Nachricht vorübergehend im Arbeitsspeicher, bevor sie in beständigen Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e2b07-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e2b07-134">-EnablePartitioning</span></span>
<span data-ttu-id="e2b07-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="e2b07-135">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-136">-ForwardDead NachredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="e2b07-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="e2b07-137">Warteschlangen-/Themenname zum Weiterleiten der Nachricht "In toter Buchstabe"</span><span class="sxs-lookup"><span data-stu-id="e2b07-137">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="e2b07-138">-ForwardTo</span></span>
<span data-ttu-id="e2b07-139">Warteschlangen-/Themenname zum Weiterleiten der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e2b07-139">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="e2b07-140">-LockDuration</span></span>
<span data-ttu-id="e2b07-141">Dauer sperren</span><span class="sxs-lookup"><span data-stu-id="e2b07-141">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e2b07-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="e2b07-143">MaxDeliveryCount – die maximale Anzahl der Zustellungen.</span><span class="sxs-lookup"><span data-stu-id="e2b07-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="e2b07-144">Eine Nachricht wird nach dieser Anzahl von Lieferungen automatisch in den In-Mail-Tod tiert.</span><span class="sxs-lookup"><span data-stu-id="e2b07-144">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e2b07-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="e2b07-146">MaxSizeInMegabytes – die maximale Größe der Warteschlange in Megabyte, d. h. die Größe des für die Warteschlange zugeordneten Arbeitsspeichers. Der Standardwert ist 1024.</span><span class="sxs-lookup"><span data-stu-id="e2b07-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="e2b07-147">Die Maximale Für Standard-SKU ist 5120 und für die Premium-SKU 81920, zulässige Werte: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="e2b07-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e2b07-148">-MessageCount</span></span>
<span data-ttu-id="e2b07-149">MessageCount – Die Anzahl der Nachrichten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e2b07-149">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-150">-Name</span><span class="sxs-lookup"><span data-stu-id="e2b07-150">-Name</span></span>
<span data-ttu-id="e2b07-151">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="e2b07-151">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2b07-152">-Namespace</span></span>
<span data-ttu-id="e2b07-153">Namespacename</span><span class="sxs-lookup"><span data-stu-id="e2b07-153">Namespace Name</span></span>

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

### <span data-ttu-id="e2b07-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="e2b07-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="e2b07-155">RequiresDuplicateDetection – ein Wert, der angibt, ob die Warteschlange das Sitzungskonzept unterstützt</span><span class="sxs-lookup"><span data-stu-id="e2b07-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="e2b07-156">-RequiresSession</span></span>
<span data-ttu-id="e2b07-157">RequiresSession – der Wert, der angibt, ob diese Warteschlange Sitzungen verwendet</span><span class="sxs-lookup"><span data-stu-id="e2b07-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b07-158">-ResourceGroupName</span></span>
<span data-ttu-id="e2b07-159">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e2b07-159">The name of the resource group</span></span>

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

### <span data-ttu-id="e2b07-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e2b07-160">-SizeInBytes</span></span>
<span data-ttu-id="e2b07-161">SizeInBytes – die Größe der Warteschlange in Bytes</span><span class="sxs-lookup"><span data-stu-id="e2b07-161">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2b07-162">-Confirm</span></span>
<span data-ttu-id="e2b07-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2b07-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-164">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e2b07-164">-WhatIf</span></span>
<span data-ttu-id="e2b07-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2b07-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b07-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2b07-166">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b07-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b07-167">CommonParameters</span></span>
<span data-ttu-id="e2b07-168">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b07-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b07-169">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b07-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b07-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2b07-170">INPUTS</span></span>

### <span data-ttu-id="e2b07-171">System.String</span><span class="sxs-lookup"><span data-stu-id="e2b07-171">System.String</span></span>

### <span data-ttu-id="e2b07-172">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2b07-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e2b07-173">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2b07-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e2b07-174">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2b07-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e2b07-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2b07-175">OUTPUTS</span></span>

### <span data-ttu-id="e2b07-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="e2b07-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="e2b07-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e2b07-177">NOTES</span></span>

## <span data-ttu-id="e2b07-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e2b07-178">RELATED LINKS</span></span>
