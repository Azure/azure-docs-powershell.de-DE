---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 87679299d17cf3e92cf6a797050c14aa65055db2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824787"
---
# <span data-ttu-id="52ce3-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="52ce3-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="52ce3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="52ce3-103">Erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="52ce3-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="52ce3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52ce3-104">SYNTAX</span></span>

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

## <span data-ttu-id="52ce3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="52ce3-106">Das Cmdlet **New-AzServiceBusQueue** erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="52ce3-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="52ce3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="52ce3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52ce3-108">Example 1</span></span>
```
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

<span data-ttu-id="52ce3-109">Erstellt eine neue ServiceBus-Warteschlange `SB-Queue_example1` im angegebenen ServiceBus-Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="52ce3-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="52ce3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="52ce3-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="52ce3-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="52ce3-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem die Warteschlange automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="52ce3-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="52ce3-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="52ce3-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="52ce3-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="52ce3-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="52ce3-115">Toter Schriftzug beim Nachrichtenablauf</span><span class="sxs-lookup"><span data-stu-id="52ce3-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="52ce3-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="52ce3-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="52ce3-117">TimeSpan to Live-Wert.</span><span class="sxs-lookup"><span data-stu-id="52ce3-117">Timespan to live value.</span></span>
<span data-ttu-id="52ce3-118">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="52ce3-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="52ce3-119">Dies ist der Standardwert, der verwendet wird, wenn TimeToLive nicht auf eine Nachricht selbst eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="52ce3-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="52ce3-120">Für Standard = TimeSpan. Max und Basic = 14 Tage</span><span class="sxs-lookup"><span data-stu-id="52ce3-120">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="52ce3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ce3-121">-DefaultProfile</span></span>
<span data-ttu-id="52ce3-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52ce3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ce3-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="52ce3-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="52ce3-124">Gibt das Zeitfenster für den doppelten Erkennungs Verlauf an, einen [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Wert, der die Dauer des doppelten Erkennungs Verlaufs definiert.</span><span class="sxs-lookup"><span data-stu-id="52ce3-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="52ce3-125">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="52ce3-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="52ce3-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="52ce3-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="52ce3-127">Aktivieren von Batchvorgängen – Wert, der angibt, ob serverseitige Batchvorgänge aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="52ce3-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="52ce3-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="52ce3-128">-EnableExpress</span></span>
<span data-ttu-id="52ce3-129">EnableExpress – ein Wert, der angibt, ob Express Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="52ce3-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="52ce3-130">Eine Express-Warteschlange speichert eine Nachricht vorübergehend im Arbeitsspeicher, bevor Sie in den dauerhaften Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="52ce3-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="52ce3-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="52ce3-131">-EnablePartitioning</span></span>
<span data-ttu-id="52ce3-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="52ce3-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="52ce3-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="52ce3-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="52ce3-134">Name der Warteschlange/des Themas zum Weiterleiten der Nachricht für unzustellbare Briefe</span><span class="sxs-lookup"><span data-stu-id="52ce3-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="52ce3-135">-Freuen</span><span class="sxs-lookup"><span data-stu-id="52ce3-135">-ForwardTo</span></span>
<span data-ttu-id="52ce3-136">Name der Warteschlange/des Themas zum Weiterleiten der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="52ce3-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="52ce3-137">-Lock Duration</span><span class="sxs-lookup"><span data-stu-id="52ce3-137">-LockDuration</span></span>
<span data-ttu-id="52ce3-138">Dauer Sperren</span><span class="sxs-lookup"><span data-stu-id="52ce3-138">Lock Duration</span></span>

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

### <span data-ttu-id="52ce3-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="52ce3-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="52ce3-140">MaxDeliveryCount – die maximale Anzahl von Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="52ce3-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="52ce3-141">Nach dieser Anzahl von Lieferungen wird automatisch eine Nachricht deadlettered.</span><span class="sxs-lookup"><span data-stu-id="52ce3-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="52ce3-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="52ce3-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="52ce3-143">MaxSizeInMegabytes – die maximale Größe der Warteschlange in Megabytes, also die Größe des Arbeitsspeichers, der für die Warteschlange reserviert ist. Standard ist 1024.</span><span class="sxs-lookup"><span data-stu-id="52ce3-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="52ce3-144">Max für Standard-SKU ist 5120 und für die Premium-SKU ist 81920, zulässige Werte: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="52ce3-144">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="52ce3-145">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="52ce3-145">-MessageCount</span></span>
<span data-ttu-id="52ce3-146">MessageCount – die Anzahl der Nachrichten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="52ce3-146">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="52ce3-147">-Name</span><span class="sxs-lookup"><span data-stu-id="52ce3-147">-Name</span></span>
<span data-ttu-id="52ce3-148">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="52ce3-148">Queue Name</span></span>

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

### <span data-ttu-id="52ce3-149">-Namespace</span><span class="sxs-lookup"><span data-stu-id="52ce3-149">-Namespace</span></span>
<span data-ttu-id="52ce3-150">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="52ce3-150">Namespace Name</span></span>

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

### <span data-ttu-id="52ce3-151">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="52ce3-151">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="52ce3-152">RequiresDuplicateDetection – ein Wert, der angibt, ob die Warteschlange das Konzept der Sitzung unterstützt</span><span class="sxs-lookup"><span data-stu-id="52ce3-152">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="52ce3-153">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="52ce3-153">-RequiresSession</span></span>
<span data-ttu-id="52ce3-154">RequiresSession – der Wert, der angibt, ob diese Warteschlange Sitzungen verwendet</span><span class="sxs-lookup"><span data-stu-id="52ce3-154">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="52ce3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ce3-155">-ResourceGroupName</span></span>
<span data-ttu-id="52ce3-156">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="52ce3-156">The name of the resource group</span></span>

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

### <span data-ttu-id="52ce3-157">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="52ce3-157">-SizeInBytes</span></span>
<span data-ttu-id="52ce3-158">SizeInBytes-die Größe der Warteschlange in Bytes</span><span class="sxs-lookup"><span data-stu-id="52ce3-158">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="52ce3-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52ce3-159">-Confirm</span></span>
<span data-ttu-id="52ce3-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52ce3-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ce3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ce3-161">-WhatIf</span></span>
<span data-ttu-id="52ce3-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52ce3-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ce3-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52ce3-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ce3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ce3-164">CommonParameters</span></span>
<span data-ttu-id="52ce3-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ce3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ce3-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ce3-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ce3-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52ce3-167">INPUTS</span></span>

### <span data-ttu-id="52ce3-168">System. String</span><span class="sxs-lookup"><span data-stu-id="52ce3-168">System.String</span></span>

### <span data-ttu-id="52ce3-169">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52ce3-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="52ce3-170">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52ce3-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="52ce3-171">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52ce3-171">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52ce3-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52ce3-172">OUTPUTS</span></span>

### <span data-ttu-id="52ce3-173">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="52ce3-173">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="52ce3-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="52ce3-174">NOTES</span></span>

## <span data-ttu-id="52ce3-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52ce3-175">RELATED LINKS</span></span>
