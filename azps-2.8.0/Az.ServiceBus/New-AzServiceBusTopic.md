---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
ms.openlocfilehash: 8fe78fff4d297233ee322b58c426099f160b2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823252"
---
# <span data-ttu-id="7d556-101">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7d556-101">New-AzServiceBusTopic</span></span>

## <span data-ttu-id="7d556-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d556-102">SYNOPSIS</span></span>
<span data-ttu-id="7d556-103">Erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7d556-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7d556-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d556-104">SYNTAX</span></span>

```
New-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d556-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d556-105">DESCRIPTION</span></span>
<span data-ttu-id="7d556-106">Das Cmdlet **New-AzServiceBusTopic** erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7d556-106">The **New-AzServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7d556-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d556-107">EXAMPLES</span></span>

### <span data-ttu-id="7d556-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d556-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="7d556-109">Erstellt ein neues Service Bus `SB-Topic_exampl1` -Thema im angegebenen ServiceBus-Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7d556-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7d556-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d556-110">PARAMETERS</span></span>

### <span data-ttu-id="7d556-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="7d556-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="7d556-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem das Thema automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7d556-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="7d556-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="7d556-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="7d556-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="7d556-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="7d556-115">Gibt die Dauer an, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d556-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="7d556-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d556-116">-DefaultProfile</span></span>
<span data-ttu-id="7d556-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d556-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d556-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="7d556-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="7d556-119">Gibt die [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Struktur an, die die Dauer des doppelten Erkennungs Verlaufs definiert.</span><span class="sxs-lookup"><span data-stu-id="7d556-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="7d556-120">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="7d556-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="7d556-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="7d556-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="7d556-122">Gibt an, ob serverseitige Batchvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7d556-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="7d556-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="7d556-123">-EnableExpress</span></span>
<span data-ttu-id="7d556-124">Gibt an, ob Express Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7d556-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="7d556-125">Eine Express-Warteschlange speichert eine Nachricht vorübergehend im Arbeitsspeicher, bevor Sie in den dauerhaften Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7d556-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="7d556-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7d556-126">-EnablePartitioning</span></span>
<span data-ttu-id="7d556-127">Gibt an, ob das Thema über mehrere nachrichtenbroker partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d556-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="7d556-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7d556-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="7d556-129">Die maximale Größe des Themas in Megabyte, also die Größe des Arbeitsspeichers, der für das Thema reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d556-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="7d556-130">-Name</span><span class="sxs-lookup"><span data-stu-id="7d556-130">-Name</span></span>
<span data-ttu-id="7d556-131">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="7d556-131">Topic Name.</span></span>

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

### <span data-ttu-id="7d556-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d556-132">-Namespace</span></span>
<span data-ttu-id="7d556-133">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="7d556-133">Namespace Name.</span></span>

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

### <span data-ttu-id="7d556-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="7d556-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="7d556-135">Gibt an, ob für das Thema Duplizierungs Erkennung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7d556-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="7d556-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d556-136">-ResourceGroupName</span></span>
<span data-ttu-id="7d556-137">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7d556-137">The name of the resource group</span></span>

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

### <span data-ttu-id="7d556-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="7d556-138">-SizeInBytes</span></span>
<span data-ttu-id="7d556-139">Gibt die Größe des Themas in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="7d556-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="7d556-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="7d556-140">-SupportOrdering</span></span>
<span data-ttu-id="7d556-141">Gibt an, ob das Thema die Reihenfolge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d556-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="7d556-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d556-142">-Confirm</span></span>
<span data-ttu-id="7d556-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d556-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d556-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d556-144">-WhatIf</span></span>
<span data-ttu-id="7d556-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d556-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d556-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d556-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d556-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d556-147">CommonParameters</span></span>
<span data-ttu-id="7d556-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d556-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d556-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d556-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d556-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d556-150">INPUTS</span></span>

### <span data-ttu-id="7d556-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7d556-151">System.String</span></span>

### <span data-ttu-id="7d556-152">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d556-152">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7d556-153">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d556-153">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7d556-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d556-154">OUTPUTS</span></span>

### <span data-ttu-id="7d556-155">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="7d556-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="7d556-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d556-156">NOTES</span></span>

## <span data-ttu-id="7d556-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d556-157">RELATED LINKS</span></span>
