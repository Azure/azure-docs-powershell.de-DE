---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367980"
---
# <span data-ttu-id="686af-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="686af-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="686af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="686af-102">SYNOPSIS</span></span>
<span data-ttu-id="686af-103">Erstellt ein Abonnement des angegebenen Servicebusthemas.</span><span class="sxs-lookup"><span data-stu-id="686af-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="686af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="686af-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="686af-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="686af-105">DESCRIPTION</span></span>
<span data-ttu-id="686af-106">Das **Cmdlet "New-AzServiceBusSubscription"** erstellt ein neues Abonnement für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="686af-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="686af-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="686af-107">EXAMPLES</span></span>

### <span data-ttu-id="686af-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="686af-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="686af-109">Erstellt das Abonnement `SB-TopicSubscription-Example1` für das angegebene Thema "Service bus". `SB-Topic_exampl1`</span><span class="sxs-lookup"><span data-stu-id="686af-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="686af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="686af-110">PARAMETERS</span></span>

### <span data-ttu-id="686af-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="686af-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="686af-112">Gibt das [TimeSpan-Leerlaufintervall](https://msdn.microsoft.com/library/system.timespan.aspx) an, nach dem das Abonnement automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="686af-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="686af-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="686af-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="686af-114">-DeadFilterringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="686af-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="686af-115">Wert, der angibt, ob für ein Abonnement Unterstützung von In-Buchstaben-Angaben bei Filterauswertungsausnahmen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="686af-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="686af-116">-DeadOleringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="686af-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="686af-117">Intschrift bei Nachrichtenablauf</span><span class="sxs-lookup"><span data-stu-id="686af-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="686af-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="686af-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="686af-119">Zeitraum bis Zum Livewert.</span><span class="sxs-lookup"><span data-stu-id="686af-119">Timespan to live value.</span></span>
<span data-ttu-id="686af-120">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Senden der Nachricht an den Service Bus.</span><span class="sxs-lookup"><span data-stu-id="686af-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="686af-121">Dies ist der Standardwert, der verwendet wird, wenn "TimeToLive" nicht für eine Nachricht selbst festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="686af-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="686af-122">Für Standard = Timespan.Max und Basic = 14 Tage</span><span class="sxs-lookup"><span data-stu-id="686af-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="686af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686af-123">-DefaultProfile</span></span>
<span data-ttu-id="686af-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="686af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="686af-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="686af-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="686af-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span><span class="sxs-lookup"><span data-stu-id="686af-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="686af-127">-ForwardDead NachredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="686af-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="686af-128">Warteschlangen-/Themenname zum Weiterleiten der Nachricht "In toter Buchstabe"</span><span class="sxs-lookup"><span data-stu-id="686af-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="686af-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="686af-129">-ForwardTo</span></span>
<span data-ttu-id="686af-130">Warteschlangen-/Themenname zum Weiterleiten der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="686af-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="686af-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="686af-131">-LockDuration</span></span>
<span data-ttu-id="686af-132">Dauer sperren</span><span class="sxs-lookup"><span data-stu-id="686af-132">Lock Duration</span></span>

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

### <span data-ttu-id="686af-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="686af-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="686af-134">MaxDeliveryCount – die maximale Anzahl der Zustellungen.</span><span class="sxs-lookup"><span data-stu-id="686af-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="686af-135">Eine Nachricht wird nach dieser Anzahl von Lieferungen automatisch in den In-Mail-Tod tiert.</span><span class="sxs-lookup"><span data-stu-id="686af-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="686af-136">-Name</span><span class="sxs-lookup"><span data-stu-id="686af-136">-Name</span></span>
<span data-ttu-id="686af-137">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="686af-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686af-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="686af-138">-Namespace</span></span>
<span data-ttu-id="686af-139">Namespacename</span><span class="sxs-lookup"><span data-stu-id="686af-139">Namespace Name</span></span>

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

### <span data-ttu-id="686af-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="686af-140">-RequiresSession</span></span>
<span data-ttu-id="686af-141">RequiresSession – der Wert, der angibt, ob für diese Warteschlange eine Duplikaterkennung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="686af-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="686af-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="686af-142">-ResourceGroupName</span></span>
<span data-ttu-id="686af-143">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="686af-143">The name of the resource group</span></span>

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

### <span data-ttu-id="686af-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="686af-144">-Topic</span></span>
<span data-ttu-id="686af-145">Themaname</span><span class="sxs-lookup"><span data-stu-id="686af-145">Topic Name</span></span>

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

### <span data-ttu-id="686af-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="686af-146">-Confirm</span></span>
<span data-ttu-id="686af-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="686af-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="686af-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="686af-148">-WhatIf</span></span>
<span data-ttu-id="686af-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="686af-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="686af-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="686af-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="686af-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686af-151">CommonParameters</span></span>
<span data-ttu-id="686af-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686af-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686af-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="686af-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686af-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="686af-154">INPUTS</span></span>

### <span data-ttu-id="686af-155">System.String</span><span class="sxs-lookup"><span data-stu-id="686af-155">System.String</span></span>

### <span data-ttu-id="686af-156">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="686af-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="686af-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="686af-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="686af-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="686af-158">OUTPUTS</span></span>

### <span data-ttu-id="686af-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="686af-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="686af-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="686af-160">NOTES</span></span>

## <span data-ttu-id="686af-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="686af-161">RELATED LINKS</span></span>
