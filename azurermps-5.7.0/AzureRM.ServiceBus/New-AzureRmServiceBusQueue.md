---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663424"
---
# <span data-ttu-id="948e6-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="948e6-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="948e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="948e6-102">SYNOPSIS</span></span>
<span data-ttu-id="948e6-103">Erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="948e6-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="948e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="948e6-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="948e6-105">DESCRIPTION</span></span>
<span data-ttu-id="948e6-106">Das Cmdlet **New-AzureRmServiceBusQueue** erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="948e6-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="948e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="948e6-107">EXAMPLES</span></span>

### <span data-ttu-id="948e6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="948e6-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="948e6-109">Erstellt eine neue ServiceBus-Warteschlange `SB-Queue_exampl1` im angegebenen ServiceBus-Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="948e6-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="948e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="948e6-110">PARAMETERS</span></span>

### <span data-ttu-id="948e6-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="948e6-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="948e6-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem die Warteschlange automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="948e6-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="948e6-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="948e6-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="948e6-114">-Confirm</span></span>
<span data-ttu-id="948e6-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="948e6-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="948e6-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="948e6-117">Toter Schriftzug beim Nachrichtenablauf</span><span class="sxs-lookup"><span data-stu-id="948e6-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="948e6-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="948e6-119">TimeSpan to Live-Wert.</span><span class="sxs-lookup"><span data-stu-id="948e6-119">Timespan to live value.</span></span>
<span data-ttu-id="948e6-120">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="948e6-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="948e6-121">Dies ist der Standardwert, der verwendet wird, wenn TimeToLive nicht auf eine Nachricht selbst eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="948e6-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="948e6-122">Für Standard = TimeSpan. Max und Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="948e6-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948e6-123">-DefaultProfile</span></span>
<span data-ttu-id="948e6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="948e6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="948e6-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="948e6-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="948e6-126">Gibt das Zeitfenster für das doppelte Erkennungsprotokoll an, ein [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -eingestellte definiert die Dauer des doppelten Erkennungs Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="948e6-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="948e6-127">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="948e6-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="948e6-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="948e6-129">Aktivieren von Batchvorgängen – Wert, der angibt, ob serverseitige Batchvorgänge aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="948e6-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="948e6-130">-EnableExpress</span></span>
<span data-ttu-id="948e6-131">EnableExpress – ein Wert, der angibt, ob Express Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="948e6-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="948e6-132">Eine Express-Warteschlange speichert eine Nachricht vorübergehend im Arbeitsspeicher, bevor Sie in den dauerhaften Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="948e6-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="948e6-133">-EnablePartitioning</span></span>
<span data-ttu-id="948e6-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="948e6-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="948e6-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="948e6-136">Name der Warteschlange/des Themas zum Weiterleiten der Nachricht für unzustellbare Briefe</span><span class="sxs-lookup"><span data-stu-id="948e6-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-137">-Freuen</span><span class="sxs-lookup"><span data-stu-id="948e6-137">-ForwardTo</span></span>
<span data-ttu-id="948e6-138">Name der Warteschlange/des Themas zum Weiterleiten der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="948e6-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-139">-Lock Duration</span><span class="sxs-lookup"><span data-stu-id="948e6-139">-LockDuration</span></span>
<span data-ttu-id="948e6-140">Dauer Sperren</span><span class="sxs-lookup"><span data-stu-id="948e6-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="948e6-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="948e6-142">MaxDeliveryCount – die maximale Anzahl von Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="948e6-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="948e6-143">Nach dieser Anzahl von Lieferungen wird automatisch eine Nachricht deadlettered.</span><span class="sxs-lookup"><span data-stu-id="948e6-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="948e6-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="948e6-145">MaxSizeInMegabytes – die maximale Größe der Warteschlange in Megabytes, also die Größe des Arbeitsspeichers, der für die Warteschlange reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="948e6-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="948e6-146">-MessageCount</span></span>
<span data-ttu-id="948e6-147">MessageCount – die Anzahl der Nachrichten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="948e6-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-148">-Name</span><span class="sxs-lookup"><span data-stu-id="948e6-148">-Name</span></span>
<span data-ttu-id="948e6-149">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="948e6-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="948e6-150">-Namespace</span></span>
<span data-ttu-id="948e6-151">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="948e6-151">Namespace Name</span></span>

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

### <span data-ttu-id="948e6-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="948e6-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="948e6-153">RequiresDuplicateDetection – ein Wert, der angibt, ob die Warteschlange das Konzept der Sitzung unterstützt</span><span class="sxs-lookup"><span data-stu-id="948e6-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="948e6-154">-RequiresSession</span></span>
<span data-ttu-id="948e6-155">RequiresSession – der Wert, der angibt, ob für diese Warteschlange eine doppelte Erkennung erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="948e6-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948e6-156">-ResourceGroupName</span></span>
<span data-ttu-id="948e6-157">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="948e6-157">The name of the resource group</span></span>

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

### <span data-ttu-id="948e6-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="948e6-158">-SizeInBytes</span></span>
<span data-ttu-id="948e6-159">SizeInBytes-die Größe der Warteschlange in Bytes</span><span class="sxs-lookup"><span data-stu-id="948e6-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948e6-160">-WhatIf</span></span>
<span data-ttu-id="948e6-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="948e6-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948e6-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="948e6-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948e6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948e6-163">CommonParameters</span></span>
<span data-ttu-id="948e6-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948e6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="948e6-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948e6-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948e6-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="948e6-166">INPUTS</span></span>

### <span data-ttu-id="948e6-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="948e6-167">-ResourceGroup</span></span>
 <span data-ttu-id="948e6-168">System. String</span><span class="sxs-lookup"><span data-stu-id="948e6-168">System.String</span></span>

### <span data-ttu-id="948e6-169">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="948e6-169">-NamespaceName</span></span>
 <span data-ttu-id="948e6-170">System. String</span><span class="sxs-lookup"><span data-stu-id="948e6-170">System.String</span></span>

### <span data-ttu-id="948e6-171">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="948e6-171">-QueueName</span></span>
 <span data-ttu-id="948e6-172">System. String</span><span class="sxs-lookup"><span data-stu-id="948e6-172">System.String</span></span>

### <span data-ttu-id="948e6-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="948e6-173">-EnablePartitioning</span></span>
 <span data-ttu-id="948e6-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="948e6-174">System.Boolean?</span></span>


## <span data-ttu-id="948e6-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="948e6-175">OUTPUTS</span></span>

### <span data-ttu-id="948e6-176">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="948e6-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="948e6-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="948e6-177">NOTES</span></span>

## <span data-ttu-id="948e6-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="948e6-178">RELATED LINKS</span></span>
