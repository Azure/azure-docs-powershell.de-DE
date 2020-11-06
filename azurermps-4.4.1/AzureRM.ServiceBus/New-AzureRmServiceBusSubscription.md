---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496854"
---
# <span data-ttu-id="8cb05-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="8cb05-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="8cb05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cb05-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb05-103">Erstellt ein Abonnement für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="8cb05-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cb05-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb05-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb05-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb05-106">Das Cmdlet **New-AzureRmServiceBusSubscription** erstellt ein neues Abonnement für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="8cb05-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="8cb05-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cb05-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb05-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cb05-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="8cb05-109">Erstellt das Abonnement `SB-TopicSubscription-Example1` für das angegebene Service Bus `SB-Topic_exampl1` -Thema.</span><span class="sxs-lookup"><span data-stu-id="8cb05-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="8cb05-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb05-110">PARAMETERS</span></span>

### <span data-ttu-id="8cb05-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="8cb05-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="8cb05-112">Gibt das [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) -Leerlaufintervall an, nach dem das Abonnement automatisch gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="8cb05-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="8cb05-113">Die Mindestdauer beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8cb05-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="8cb05-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="8cb05-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="8cb05-115">Gibt an, ob ein Abonnement für Filter Auswertungs Ausnahmen eine Dead Letter-Unterstützung aufweist.</span><span class="sxs-lookup"><span data-stu-id="8cb05-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="8cb05-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="8cb05-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="8cb05-117">Gibt an, ob ein Abonnement DeadLetter-Unterstützung hat, wenn eine Nachricht abläuft.</span><span class="sxs-lookup"><span data-stu-id="8cb05-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="8cb05-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="8cb05-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="8cb05-119">Gibt an, ob serverseitige Batchvorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="8cb05-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="8cb05-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="8cb05-120">-IsReadOnly</span></span>
<span data-ttu-id="8cb05-121">Gibt an, ob die Entitäts Beschreibung schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="8cb05-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="8cb05-122">-Lock Duration</span><span class="sxs-lookup"><span data-stu-id="8cb05-122">-LockDuration</span></span>
<span data-ttu-id="8cb05-123">Gibt die Zeitspanne für die Sperrdauer für das Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="8cb05-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="8cb05-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="8cb05-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="8cb05-125">Gibt die Anzahl der maximalen Lieferungen an.</span><span class="sxs-lookup"><span data-stu-id="8cb05-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="8cb05-126">Nach dieser Anzahl von Lieferungen wird automatisch eine Nachricht deadlettered.</span><span class="sxs-lookup"><span data-stu-id="8cb05-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="8cb05-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="8cb05-127">-RequiresSession</span></span>
<span data-ttu-id="8cb05-128">Gibt an, ob ein Abonnement das Konzept von Sitzungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb05-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="8cb05-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cb05-129">-Confirm</span></span>
<span data-ttu-id="8cb05-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cb05-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb05-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb05-131">-WhatIf</span></span>
<span data-ttu-id="8cb05-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb05-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cb05-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb05-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cb05-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="8cb05-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="8cb05-135">TimeSpan to Live-Wert.</span><span class="sxs-lookup"><span data-stu-id="8cb05-135">Timespan to live value.</span></span> <span data-ttu-id="8cb05-136">Dies ist die Dauer, nach der die Nachricht abläuft, beginnend mit dem Zeitpunkt, zu dem die Nachricht an Service Bus gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cb05-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="8cb05-137">Dies ist der Standardwert, der verwendet wird, wenn TimeToLive nicht auf eine Nachricht selbst eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="8cb05-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="8cb05-138">Für Standard = TimeSpan. Max und Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="8cb05-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="8cb05-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb05-139">-DefaultProfile</span></span>
<span data-ttu-id="8cb05-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cb05-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb05-141">-Name</span><span class="sxs-lookup"><span data-stu-id="8cb05-141">-Name</span></span>
<span data-ttu-id="8cb05-142">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="8cb05-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb05-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8cb05-143">-Namespace</span></span>
<span data-ttu-id="8cb05-144">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8cb05-144">Namespace Name.</span></span>

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

### <span data-ttu-id="8cb05-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb05-145">-ResourceGroupName</span></span>
<span data-ttu-id="8cb05-146">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8cb05-146">The name of the resource group</span></span>

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

### <span data-ttu-id="8cb05-147">-Topic</span><span class="sxs-lookup"><span data-stu-id="8cb05-147">-Topic</span></span>
<span data-ttu-id="8cb05-148">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="8cb05-148">Topic Name.</span></span>

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

### <span data-ttu-id="8cb05-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb05-149">CommonParameters</span></span>
<span data-ttu-id="8cb05-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb05-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb05-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb05-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb05-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cb05-152">INPUTS</span></span>

### <span data-ttu-id="8cb05-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cb05-153">-ResourceGroup</span></span>
 <span data-ttu-id="8cb05-154">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb05-154">System.String</span></span>
 

### <span data-ttu-id="8cb05-155">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="8cb05-155">-NamespaceName</span></span>
 <span data-ttu-id="8cb05-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb05-156">System.String</span></span>
 

### <span data-ttu-id="8cb05-157">-Topicname</span><span class="sxs-lookup"><span data-stu-id="8cb05-157">-TopicName</span></span>
 <span data-ttu-id="8cb05-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb05-158">System.String</span></span>
 

### <span data-ttu-id="8cb05-159">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="8cb05-159">-SubscriptionName</span></span>
 <span data-ttu-id="8cb05-160">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb05-160">System.String</span></span>

## <span data-ttu-id="8cb05-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cb05-161">OUTPUTS</span></span>

### <span data-ttu-id="8cb05-162">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="8cb05-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="8cb05-163">Name: SB-TopicSubscription-beispiel1 Ort: West-US-AccessedAt: 1/20/2017 3:18:54 am AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 am DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: available IsReadOnly: Lock Duration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: Falscher Status: Active UpdatedAt: 1/20/2017 3:18:54 am</span><span class="sxs-lookup"><span data-stu-id="8cb05-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="8cb05-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cb05-164">NOTES</span></span>

## <span data-ttu-id="8cb05-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cb05-165">RELATED LINKS</span></span>

