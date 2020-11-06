---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: e2ca0b6902ecc13c9dfe4f418ea5d321b6e36dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482046"
---
# <span data-ttu-id="65786-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="65786-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="65786-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65786-102">SYNOPSIS</span></span>
<span data-ttu-id="65786-103">Erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="65786-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65786-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65786-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65786-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65786-105">DESCRIPTION</span></span>
<span data-ttu-id="65786-106">Das Cmdlet **New-AzureRmServiceBusTopic** erstellt ein neues Service Bus-Thema im angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="65786-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="65786-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65786-107">EXAMPLES</span></span>

### <span data-ttu-id="65786-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65786-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

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

<span data-ttu-id="65786-109">Erstellt ein neues Service Bus `SB-Topic_exampl1` -Thema im angegebenen ServiceBus-Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="65786-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="65786-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65786-110">PARAMETERS</span></span>

### <span data-ttu-id="65786-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="65786-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="65786-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem das Thema automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="65786-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="65786-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="65786-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="65786-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="65786-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="65786-115">Gibt die Dauer an, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="65786-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="65786-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65786-116">-DefaultProfile</span></span>
<span data-ttu-id="65786-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65786-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65786-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="65786-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="65786-119">Gibt die [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Struktur an, die die Dauer des doppelten Erkennungs Verlaufs definiert.</span><span class="sxs-lookup"><span data-stu-id="65786-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="65786-120">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="65786-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="65786-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="65786-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="65786-122">Gibt an, ob serverseitige Batchvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="65786-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="65786-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="65786-123">-EnableExpress</span></span>
<span data-ttu-id="65786-124">Gibt an, ob Express Entitäten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="65786-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="65786-125">Eine Express-Warteschlange speichert eine Nachricht vorübergehend im Arbeitsspeicher, bevor Sie in den dauerhaften Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="65786-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="65786-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="65786-126">-EnablePartitioning</span></span>
<span data-ttu-id="65786-127">Gibt an, ob das Thema über mehrere nachrichtenbroker partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65786-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="65786-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="65786-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="65786-129">Die maximale Größe des Themas in Megabyte, also die Größe des Arbeitsspeichers, der für das Thema reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="65786-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="65786-130">-Name</span><span class="sxs-lookup"><span data-stu-id="65786-130">-Name</span></span>
<span data-ttu-id="65786-131">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="65786-131">Topic Name.</span></span>

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

### <span data-ttu-id="65786-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65786-132">-Namespace</span></span>
<span data-ttu-id="65786-133">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="65786-133">Namespace Name.</span></span>

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

### <span data-ttu-id="65786-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="65786-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="65786-135">Gibt an, ob für das Thema Duplizierungs Erkennung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="65786-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="65786-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65786-136">-ResourceGroupName</span></span>
<span data-ttu-id="65786-137">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="65786-137">The name of the resource group</span></span>

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

### <span data-ttu-id="65786-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="65786-138">-SizeInBytes</span></span>
<span data-ttu-id="65786-139">Gibt die Größe des Themas in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="65786-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="65786-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="65786-140">-SupportOrdering</span></span>
<span data-ttu-id="65786-141">Gibt an, ob das Thema die Reihenfolge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65786-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="65786-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65786-142">-Confirm</span></span>
<span data-ttu-id="65786-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65786-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65786-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65786-144">-WhatIf</span></span>
<span data-ttu-id="65786-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65786-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65786-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65786-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65786-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65786-147">CommonParameters</span></span>
<span data-ttu-id="65786-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65786-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65786-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65786-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65786-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65786-150">INPUTS</span></span>

### <span data-ttu-id="65786-151">System. String</span><span class="sxs-lookup"><span data-stu-id="65786-151">System.String</span></span>

### <span data-ttu-id="65786-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="65786-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="65786-153">System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="65786-153">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="65786-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65786-154">OUTPUTS</span></span>

### <span data-ttu-id="65786-155">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="65786-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="65786-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="65786-156">NOTES</span></span>

## <span data-ttu-id="65786-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65786-157">RELATED LINKS</span></span>
