---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481602"
---
# <span data-ttu-id="7caa7-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7caa7-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="7caa7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7caa7-102">SYNOPSIS</span></span>
<span data-ttu-id="7caa7-103">Erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7caa7-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7caa7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7caa7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7caa7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7caa7-105">DESCRIPTION</span></span>
<span data-ttu-id="7caa7-106">Das Cmdlet **New-AzureRmServiceBusTopic** erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7caa7-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7caa7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7caa7-107">EXAMPLES</span></span>

### <span data-ttu-id="7caa7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7caa7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="7caa7-109">Erstellt ein neues Service Bus `SB-Topic_exampl1` -Thema im angegebenen ServiceBus-Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7caa7-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7caa7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7caa7-110">PARAMETERS</span></span>

### <span data-ttu-id="7caa7-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="7caa7-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="7caa7-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem das Thema automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7caa7-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="7caa7-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="7caa7-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="7caa7-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="7caa7-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="7caa7-115">Gibt die Dauer an, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7caa7-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="7caa7-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="7caa7-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="7caa7-117">Gibt die [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Struktur an, die die Dauer des doppelten Erkennungs Verlaufs definiert.</span><span class="sxs-lookup"><span data-stu-id="7caa7-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="7caa7-118">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="7caa7-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="7caa7-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="7caa7-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="7caa7-120">Gibt an, ob serverseitige Batchvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7caa7-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="7caa7-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="7caa7-121">-EnableExpress</span></span>
<span data-ttu-id="7caa7-122">Gibt an, ob Express Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7caa7-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="7caa7-123">Eine Express-Warteschlange speichert eine Nachricht vorübergehend im Arbeitsspeicher, bevor Sie in den dauerhaften Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7caa7-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="7caa7-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7caa7-124">-EnablePartitioning</span></span>
<span data-ttu-id="7caa7-125">Gibt an, ob das Thema über mehrere nachrichtenbroker partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7caa7-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="7caa7-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="7caa7-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="7caa7-127">Gibt an, ob die Abonnementpartitionierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7caa7-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="7caa7-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="7caa7-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="7caa7-129">Gibt an, ob die Filterung für Nachrichten vor der Veröffentlichung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7caa7-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="7caa7-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="7caa7-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="7caa7-131">Gibt an, ob die Nachricht den anonymen Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="7caa7-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="7caa7-132">-ISEXpress</span><span class="sxs-lookup"><span data-stu-id="7caa7-132">-IsExpress</span></span>
<span data-ttu-id="7caa7-133">Gibt an, ob das Thema Express aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7caa7-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="7caa7-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7caa7-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="7caa7-135">Die maximale Größe des Themas in Megabyte, also die Größe des Arbeitsspeichers, der für das Thema reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="7caa7-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="7caa7-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="7caa7-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="7caa7-137">Gibt an, ob für das Thema Duplizierungs Erkennung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7caa7-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="7caa7-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="7caa7-138">-SizeInBytes</span></span>
<span data-ttu-id="7caa7-139">Gibt die Größe des Themas in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="7caa7-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="7caa7-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="7caa7-140">-SupportOrdering</span></span>
<span data-ttu-id="7caa7-141">Gibt an, ob das Thema die Reihenfolge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7caa7-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="7caa7-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7caa7-142">-Confirm</span></span>
<span data-ttu-id="7caa7-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7caa7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7caa7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7caa7-144">-WhatIf</span></span>
<span data-ttu-id="7caa7-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7caa7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7caa7-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7caa7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7caa7-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7caa7-147">-DefaultProfile</span></span>
<span data-ttu-id="7caa7-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7caa7-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7caa7-149">-Name</span><span class="sxs-lookup"><span data-stu-id="7caa7-149">-Name</span></span>
<span data-ttu-id="7caa7-150">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="7caa7-150">Topic Name.</span></span>

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

### <span data-ttu-id="7caa7-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7caa7-151">-Namespace</span></span>
<span data-ttu-id="7caa7-152">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="7caa7-152">Namespace Name.</span></span>

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

### <span data-ttu-id="7caa7-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7caa7-153">-ResourceGroupName</span></span>
<span data-ttu-id="7caa7-154">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7caa7-154">The name of the resource group</span></span>

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

### <span data-ttu-id="7caa7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7caa7-155">CommonParameters</span></span>
<span data-ttu-id="7caa7-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7caa7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7caa7-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7caa7-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7caa7-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7caa7-158">INPUTS</span></span>

### <span data-ttu-id="7caa7-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7caa7-159">System.String</span></span>
<span data-ttu-id="7caa7-160">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="7caa7-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="7caa7-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7caa7-161">-ResourceGroup</span></span>
 <span data-ttu-id="7caa7-162">System. String</span><span class="sxs-lookup"><span data-stu-id="7caa7-162">System.String</span></span>

### <span data-ttu-id="7caa7-163">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="7caa7-163">-NamespaceName</span></span>
 <span data-ttu-id="7caa7-164">System. String</span><span class="sxs-lookup"><span data-stu-id="7caa7-164">System.String</span></span>

### <span data-ttu-id="7caa7-165">-Topicname</span><span class="sxs-lookup"><span data-stu-id="7caa7-165">-TopicName</span></span>
 <span data-ttu-id="7caa7-166">System. String</span><span class="sxs-lookup"><span data-stu-id="7caa7-166">System.String</span></span>

### <span data-ttu-id="7caa7-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7caa7-167">-EnablePartitioning</span></span>
 <span data-ttu-id="7caa7-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="7caa7-168">System.Boolean?</span></span>

## <span data-ttu-id="7caa7-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7caa7-169">OUTPUTS</span></span>

### <span data-ttu-id="7caa7-170">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="7caa7-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="7caa7-171">Name: SB-Topic_exampl1 Ort: West US ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/topics/S B-Topic_exampl1 Typ: Microsoft. ServiceBus/Topic AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 am CountDetails: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false ISEXpress: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false sizeInBytes: 0 Status: SubscriptionCount: SupportOrdering: false UpdatedAt: 1/20/2017 3:16:43</span><span class="sxs-lookup"><span data-stu-id="7caa7-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="7caa7-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="7caa7-172">NOTES</span></span>

## <span data-ttu-id="7caa7-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7caa7-173">RELATED LINKS</span></span>

