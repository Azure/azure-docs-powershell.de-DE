---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478937"
---
# <span data-ttu-id="f5982-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f5982-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="f5982-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5982-102">SYNOPSIS</span></span>
<span data-ttu-id="f5982-103">Erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f5982-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5982-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5982-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5982-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5982-105">DESCRIPTION</span></span>
<span data-ttu-id="f5982-106">Das Cmdlet **New-AzureRmServiceBusQueue** erstellt eine ServiceBus-Warteschlange im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f5982-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f5982-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5982-107">EXAMPLES</span></span>

### <span data-ttu-id="f5982-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5982-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="f5982-109">Erstellt eine neue ServiceBus-Warteschlange `SB-Queue_exampl1` im angegebenen ServiceBus-Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f5982-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f5982-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5982-110">PARAMETERS</span></span>

### <span data-ttu-id="f5982-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="f5982-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="f5982-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem die Warteschlange automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f5982-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="f5982-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="f5982-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="f5982-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="f5982-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="f5982-115">Gibt an, ob Nachrichten beim Ablauf deadlettered werden.</span><span class="sxs-lookup"><span data-stu-id="f5982-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="f5982-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="f5982-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="f5982-117">Gibt die standardmäßige Gültigkeitsdauer von Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="f5982-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="f5982-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="f5982-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="f5982-119">Gibt das Zeitfenster für das doppelte Erkennungsprotokoll an, ein [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -eingestellte definiert die Dauer des doppelten Erkennungs Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="f5982-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="f5982-120">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="f5982-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="f5982-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="f5982-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="f5982-122">Gibt an, ob serverseitige Batchvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="f5982-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="f5982-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="f5982-123">-EnableExpress</span></span>
<span data-ttu-id="f5982-124">Gibt an, ob Express Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="f5982-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="f5982-125">Eine Express-Warteschlange speichert eine Nachricht vorübergehend im Arbeitsspeicher, bevor Sie in den dauerhaften Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f5982-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="f5982-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="f5982-126">-EnablePartitioning</span></span>
<span data-ttu-id="f5982-127">Gibt an, ob EnablePartitioning aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5982-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5982-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="f5982-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="f5982-129">Gibt an, ob die Nachricht anonym zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="f5982-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="f5982-130">-Lock Duration</span><span class="sxs-lookup"><span data-stu-id="f5982-130">-LockDuration</span></span>
<span data-ttu-id="f5982-131">Gibt die Sperrdauer an.</span><span class="sxs-lookup"><span data-stu-id="f5982-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="f5982-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="f5982-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="f5982-133">Gibt die maximale Anzahl von Lieferungen an.</span><span class="sxs-lookup"><span data-stu-id="f5982-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="f5982-134">Nach dieser Anzahl von Lieferungen wird automatisch eine Nachricht deadlettered.</span><span class="sxs-lookup"><span data-stu-id="f5982-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="f5982-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f5982-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="f5982-136">Gibt die maximale Größe der Warteschlange in Megabyte an, also die Größe des Arbeitsspeichers, der für die Warteschlange reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5982-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="f5982-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="f5982-137">-MessageCount</span></span>
<span data-ttu-id="f5982-138">Gibt die Anzahl der Nachrichten in der Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="f5982-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="f5982-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="f5982-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="f5982-140">Gibt an, ob für die Warteschlange doppelte Erkennung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f5982-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="f5982-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="f5982-141">-RequiresSession</span></span>
<span data-ttu-id="f5982-142">Gibt an, ob diese Warteschlange Sitzungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5982-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="f5982-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="f5982-143">-SizeInBytes</span></span>
<span data-ttu-id="f5982-144">Die Größe der Warteschlange in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f5982-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="f5982-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5982-145">-Confirm</span></span>
<span data-ttu-id="f5982-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5982-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5982-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5982-147">-WhatIf</span></span>
<span data-ttu-id="f5982-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5982-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5982-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5982-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5982-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5982-150">-DefaultProfile</span></span>
<span data-ttu-id="f5982-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5982-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5982-152">-Name</span><span class="sxs-lookup"><span data-stu-id="f5982-152">-Name</span></span>
<span data-ttu-id="f5982-153">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="f5982-153">Queue Name.</span></span>

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

### <span data-ttu-id="f5982-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5982-154">-Namespace</span></span>
<span data-ttu-id="f5982-155">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="f5982-155">Namespace Name.</span></span>

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

### <span data-ttu-id="f5982-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5982-156">-ResourceGroupName</span></span>
<span data-ttu-id="f5982-157">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f5982-157">The name of the resource group</span></span>

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

### <span data-ttu-id="f5982-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5982-158">CommonParameters</span></span>
<span data-ttu-id="f5982-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5982-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5982-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5982-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5982-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5982-161">INPUTS</span></span>

### <span data-ttu-id="f5982-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5982-162">-ResourceGroup</span></span>
 <span data-ttu-id="f5982-163">System. String</span><span class="sxs-lookup"><span data-stu-id="f5982-163">System.String</span></span>

### <span data-ttu-id="f5982-164">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="f5982-164">-NamespaceName</span></span>
 <span data-ttu-id="f5982-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f5982-165">System.String</span></span>

### <span data-ttu-id="f5982-166">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="f5982-166">-QueueName</span></span>
 <span data-ttu-id="f5982-167">System. String</span><span class="sxs-lookup"><span data-stu-id="f5982-167">System.String</span></span>

### <span data-ttu-id="f5982-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="f5982-168">-EnablePartitioning</span></span>
 <span data-ttu-id="f5982-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="f5982-169">System.Boolean?</span></span>

## <span data-ttu-id="f5982-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5982-170">OUTPUTS</span></span>

### <span data-ttu-id="f5982-171">Microsoft. Azure. Commands. ServiceBus. Models. Queue Attributes</span><span class="sxs-lookup"><span data-stu-id="f5982-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="f5982-172">Name: SB-Queue_exampl1 Ort: West US Lock Duration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 am DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: DeadLetteringOnMessageExpiration: EnableExpress: EnablePartitioning IsAnonymousAccessible: MaxDeliveryCount: MaxSizeInMegabytes: MessageCount CountDetails: 16384 RequiresDuplicateDetection: RequiresSession sizeInBytes: SupportOrdering: UpdatedAt: false: false 1/20/2017 2:51:37:::</span><span class="sxs-lookup"><span data-stu-id="f5982-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="f5982-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5982-173">NOTES</span></span>

## <span data-ttu-id="f5982-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5982-174">RELATED LINKS</span></span>

