---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663423"
---
# <span data-ttu-id="4e72d-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4e72d-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="4e72d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e72d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e72d-103">Erstellt ein Abonnement für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="4e72d-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e72d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e72d-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e72d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e72d-105">DESCRIPTION</span></span>
<span data-ttu-id="4e72d-106">Das Cmdlet **New-AzureRmServiceBusSubscription** erstellt ein neues Abonnement für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="4e72d-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="4e72d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e72d-107">EXAMPLES</span></span>

### <span data-ttu-id="4e72d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e72d-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="4e72d-109">Erstellt das Abonnement `SB-TopicSubscription-Example1` für das angegebene Service Bus `SB-Topic_exampl1` -Thema.</span><span class="sxs-lookup"><span data-stu-id="4e72d-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="4e72d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e72d-110">PARAMETERS</span></span>

### <span data-ttu-id="4e72d-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="4e72d-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="4e72d-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem das Abonnement automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="4e72d-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="4e72d-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="4e72d-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="4e72d-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e72d-114">-Confirm</span></span>
<span data-ttu-id="4e72d-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e72d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e72d-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="4e72d-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="4e72d-117">Wert, der angibt, ob ein Abonnement für Filter Auswertungs Ausnahmen eine Dead Letter-Unterstützung aufweist.</span><span class="sxs-lookup"><span data-stu-id="4e72d-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="4e72d-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="4e72d-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="4e72d-119">Toter Schriftzug beim Nachrichtenablauf</span><span class="sxs-lookup"><span data-stu-id="4e72d-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="4e72d-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="4e72d-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="4e72d-121">TimeSpan to Live-Wert.</span><span class="sxs-lookup"><span data-stu-id="4e72d-121">Timespan to live value.</span></span>
<span data-ttu-id="4e72d-122">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e72d-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="4e72d-123">Dies ist der Standardwert, der verwendet wird, wenn TimeToLive nicht auf eine Nachricht selbst eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="4e72d-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="4e72d-124">Für Standard = TimeSpan. Max und Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="4e72d-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="4e72d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e72d-125">-DefaultProfile</span></span>
<span data-ttu-id="4e72d-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e72d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e72d-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="4e72d-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="4e72d-128">Aktivieren von Batchvorgängen – Wert, der angibt, ob serverseitige Batchvorgänge aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="4e72d-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="4e72d-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="4e72d-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="4e72d-130">Name der Warteschlange/des Themas zum Weiterleiten der Nachricht für unzustellbare Briefe</span><span class="sxs-lookup"><span data-stu-id="4e72d-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="4e72d-131">-Freuen</span><span class="sxs-lookup"><span data-stu-id="4e72d-131">-ForwardTo</span></span>
<span data-ttu-id="4e72d-132">Name der Warteschlange/des Themas zum Weiterleiten der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="4e72d-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="4e72d-133">-Lock Duration</span><span class="sxs-lookup"><span data-stu-id="4e72d-133">-LockDuration</span></span>
<span data-ttu-id="4e72d-134">Dauer Sperren</span><span class="sxs-lookup"><span data-stu-id="4e72d-134">Lock Duration</span></span>

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

### <span data-ttu-id="4e72d-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="4e72d-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="4e72d-136">MaxDeliveryCount – die maximale Anzahl von Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="4e72d-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="4e72d-137">Nach dieser Anzahl von Lieferungen wird automatisch eine Nachricht deadlettered.</span><span class="sxs-lookup"><span data-stu-id="4e72d-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="4e72d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4e72d-138">-Name</span></span>
<span data-ttu-id="4e72d-139">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="4e72d-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e72d-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e72d-140">-Namespace</span></span>
<span data-ttu-id="4e72d-141">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4e72d-141">Namespace Name</span></span>

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

### <span data-ttu-id="4e72d-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="4e72d-142">-RequiresSession</span></span>
<span data-ttu-id="4e72d-143">RequiresSession – der Wert, der angibt, ob für diese Warteschlange eine doppelte Erkennung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4e72d-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="4e72d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e72d-144">-ResourceGroupName</span></span>
<span data-ttu-id="4e72d-145">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4e72d-145">The name of the resource group</span></span>

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

### <span data-ttu-id="4e72d-146">-Topic</span><span class="sxs-lookup"><span data-stu-id="4e72d-146">-Topic</span></span>
<span data-ttu-id="4e72d-147">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="4e72d-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e72d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e72d-148">-WhatIf</span></span>
<span data-ttu-id="4e72d-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e72d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e72d-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e72d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e72d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e72d-151">CommonParameters</span></span>
<span data-ttu-id="4e72d-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e72d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4e72d-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e72d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e72d-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e72d-154">INPUTS</span></span>

### <span data-ttu-id="4e72d-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4e72d-155">-ResourceGroup</span></span>
 <span data-ttu-id="4e72d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4e72d-156">System.String</span></span>
 

### <span data-ttu-id="4e72d-157">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="4e72d-157">-NamespaceName</span></span>
 <span data-ttu-id="4e72d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4e72d-158">System.String</span></span>
 

### <span data-ttu-id="4e72d-159">-Topicname</span><span class="sxs-lookup"><span data-stu-id="4e72d-159">-TopicName</span></span>
 <span data-ttu-id="4e72d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="4e72d-160">System.String</span></span>
 

### <span data-ttu-id="4e72d-161">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="4e72d-161">-SubscriptionName</span></span>
 <span data-ttu-id="4e72d-162">System. String</span><span class="sxs-lookup"><span data-stu-id="4e72d-162">System.String</span></span>


## <span data-ttu-id="4e72d-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e72d-163">OUTPUTS</span></span>

### <span data-ttu-id="4e72d-164">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4e72d-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="4e72d-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e72d-165">NOTES</span></span>

## <span data-ttu-id="4e72d-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e72d-166">RELATED LINKS</span></span>
