---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 1d197683e1459173d96958199ad08b437d1d9e04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943504"
---
# <span data-ttu-id="1439a-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="1439a-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="1439a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1439a-102">SYNOPSIS</span></span>
<span data-ttu-id="1439a-103">Erstellt eine Dienstbuswarteschlange im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1439a-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1439a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1439a-104">SYNTAX</span></span>

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

## <span data-ttu-id="1439a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1439a-105">DESCRIPTION</span></span>
<span data-ttu-id="1439a-106">Das **Cmdlet New-AzServiceBusQueue** erstellt eine Dienstbuswarteschlange im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1439a-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1439a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1439a-107">EXAMPLES</span></span>

### <span data-ttu-id="1439a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1439a-108">Example 1</span></span>
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

<span data-ttu-id="1439a-109">Erstellt eine neue Service Bus-Warteschlange `SB-Queue_example1` im angegebenen Service Bus-Namespace. `SB-Example1`</span><span class="sxs-lookup"><span data-stu-id="1439a-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="1439a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1439a-110">Example 2</span></span>

<span data-ttu-id="1439a-111">Erstellt eine Dienstbuswarteschlange im angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1439a-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="1439a-112">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="1439a-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="1439a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1439a-113">PARAMETERS</span></span>

### <span data-ttu-id="1439a-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="1439a-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="1439a-115">Gibt das [](https://msdn.microsoft.com/library/system.timespan.aspx) Zeitspanne-Leerlaufintervall an, nach dem die Warteschlange automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1439a-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="1439a-116">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="1439a-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="1439a-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="1439a-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="1439a-118">Toter Schriftzug beim Ablauf der Nachricht</span><span class="sxs-lookup"><span data-stu-id="1439a-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="1439a-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="1439a-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="1439a-120">Zeitspanne zum Livewert.</span><span class="sxs-lookup"><span data-stu-id="1439a-120">Timespan to live value.</span></span>
<span data-ttu-id="1439a-121">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Senden der Nachricht an Service Bus.</span><span class="sxs-lookup"><span data-stu-id="1439a-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="1439a-122">Dies ist der Standardwert, der verwendet wird, wenn TimeToLive nicht für eine Nachricht selbst festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1439a-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="1439a-123">Für Standard = Timespan.Max und Basic = 14 Tage</span><span class="sxs-lookup"><span data-stu-id="1439a-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="1439a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1439a-124">-DefaultProfile</span></span>
<span data-ttu-id="1439a-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1439a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1439a-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="1439a-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="1439a-127">Gibt das Zeitfenster für den Doppelten Erkennungsverlauf an, einen [TimeSpan-Wert,](https://msdn.microsoft.com/library/system.timespan.aspx) der die Dauer des Duplikaterkennungsverlaufs definiert.</span><span class="sxs-lookup"><span data-stu-id="1439a-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="1439a-128">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="1439a-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="1439a-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="1439a-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="1439a-130">Aktivieren von Batchvorgängen – Wert, der angibt, ob serverseitige Batchvorgänge aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="1439a-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="1439a-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="1439a-131">-EnableExpress</span></span>
<span data-ttu-id="1439a-132">EnableExpress – ein Wert, der angibt, ob Express-Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1439a-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="1439a-133">Eine Expresswarteschlange hält eine Nachricht vorübergehend im Arbeitsspeicher, bevor sie in beständigen Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1439a-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="1439a-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="1439a-134">-EnablePartitioning</span></span>
<span data-ttu-id="1439a-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="1439a-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="1439a-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="1439a-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="1439a-137">Queue/Topic name to forward the Dead Letter message</span><span class="sxs-lookup"><span data-stu-id="1439a-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="1439a-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="1439a-138">-ForwardTo</span></span>
<span data-ttu-id="1439a-139">Name der Warteschlange/des Themas zum Weiterleiten der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1439a-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="1439a-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="1439a-140">-LockDuration</span></span>
<span data-ttu-id="1439a-141">Sperrdauer</span><span class="sxs-lookup"><span data-stu-id="1439a-141">Lock Duration</span></span>

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

### <span data-ttu-id="1439a-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="1439a-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="1439a-143">MaxDeliveryCount – die maximale Zustellungsanzahl.</span><span class="sxs-lookup"><span data-stu-id="1439a-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="1439a-144">Eine Nachricht wird nach dieser Anzahl von Lieferungen automatisch nicht mehr gesendet.</span><span class="sxs-lookup"><span data-stu-id="1439a-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="1439a-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="1439a-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="1439a-146">MaxSizeInMegabytes – die maximale Größe der Warteschlange in Megabyte, d. h. die Größe des Für die Warteschlange zugewiesenen Arbeitsspeichers. Der Standardwert ist 1024.</span><span class="sxs-lookup"><span data-stu-id="1439a-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="1439a-147">Max. für Standard-SKU ist 5120 und für Premium-SKU 81920, Zulässige Werte: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="1439a-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="1439a-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="1439a-148">-MessageCount</span></span>
<span data-ttu-id="1439a-149">MessageCount – Die Anzahl der Nachrichten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="1439a-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="1439a-150">-Name</span><span class="sxs-lookup"><span data-stu-id="1439a-150">-Name</span></span>
<span data-ttu-id="1439a-151">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="1439a-151">Queue Name</span></span>

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

### <span data-ttu-id="1439a-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1439a-152">-Namespace</span></span>
<span data-ttu-id="1439a-153">Namespacename</span><span class="sxs-lookup"><span data-stu-id="1439a-153">Namespace Name</span></span>

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

### <span data-ttu-id="1439a-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="1439a-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="1439a-155">RequiresDuplicateDetection – ein Wert, der angibt, ob die Warteschlange das Konzept der Sitzung unterstützt</span><span class="sxs-lookup"><span data-stu-id="1439a-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="1439a-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="1439a-156">-RequiresSession</span></span>
<span data-ttu-id="1439a-157">RequiresSession – der Wert, der angibt, ob diese Warteschlange Sitzungen verwendet</span><span class="sxs-lookup"><span data-stu-id="1439a-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="1439a-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1439a-158">-ResourceGroupName</span></span>
<span data-ttu-id="1439a-159">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1439a-159">The name of the resource group</span></span>

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

### <span data-ttu-id="1439a-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1439a-160">-SizeInBytes</span></span>
<span data-ttu-id="1439a-161">SizeInBytes – die Größe der Warteschlange in Bytes</span><span class="sxs-lookup"><span data-stu-id="1439a-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="1439a-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1439a-162">-Confirm</span></span>
<span data-ttu-id="1439a-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1439a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1439a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1439a-164">-WhatIf</span></span>
<span data-ttu-id="1439a-165">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1439a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1439a-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1439a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1439a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1439a-167">CommonParameters</span></span>
<span data-ttu-id="1439a-168">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1439a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1439a-169">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1439a-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1439a-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1439a-170">INPUTS</span></span>

### <span data-ttu-id="1439a-171">System.String</span><span class="sxs-lookup"><span data-stu-id="1439a-171">System.String</span></span>

### <span data-ttu-id="1439a-172">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1439a-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1439a-173">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1439a-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1439a-174">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1439a-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1439a-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1439a-175">OUTPUTS</span></span>

### <span data-ttu-id="1439a-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="1439a-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="1439a-177">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1439a-177">NOTES</span></span>

## <span data-ttu-id="1439a-178">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1439a-178">RELATED LINKS</span></span>
