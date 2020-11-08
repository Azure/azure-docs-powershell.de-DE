---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0f767b2c59a7cbf297c652873d4be1c064aec296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995797"
---
# <span data-ttu-id="4e906-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4e906-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="4e906-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e906-102">SYNOPSIS</span></span>
<span data-ttu-id="4e906-103">Entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="4e906-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4e906-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e906-104">SYNTAX</span></span>

### <span data-ttu-id="4e906-105">SubscriptionPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e906-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e906-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e906-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e906-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e906-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e906-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e906-108">DESCRIPTION</span></span>
<span data-ttu-id="4e906-109">Das Cmdlet **Remove-AzServiceBusSubscription** entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="4e906-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4e906-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e906-110">EXAMPLES</span></span>

### <span data-ttu-id="4e906-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e906-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="4e906-112">Entfernt das Abonnement `SB-TopicSubscription-Example1` für das Thema `SB-Topic_exampl1` im angegebenen ServiceBus `SB-Example1` -Namespace.</span><span class="sxs-lookup"><span data-stu-id="4e906-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="4e906-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="4e906-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="4e906-114">Beispiel 2,2-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="4e906-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="4e906-115">Beispiel 3,1-Resourcen-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="4e906-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="4e906-116">Beispiel 3,2-Resourcen-using-Zeichenfolgenwert:</span><span class="sxs-lookup"><span data-stu-id="4e906-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="4e906-117">Entfernt das Abonnement, das über die Arm-ID bereitgestellt wird, in $ResourceId/String for-Resourcen-Parameter</span><span class="sxs-lookup"><span data-stu-id="4e906-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="4e906-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e906-118">PARAMETERS</span></span>

### <span data-ttu-id="4e906-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e906-119">-AsJob</span></span>
<span data-ttu-id="4e906-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4e906-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e906-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e906-121">-DefaultProfile</span></span>
<span data-ttu-id="4e906-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e906-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e906-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e906-123">-InputObject</span></span>
<span data-ttu-id="4e906-124">Service Bus-Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="4e906-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4e906-125">-Name</span></span>
<span data-ttu-id="4e906-126">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="4e906-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e906-127">-Namespace</span></span>
<span data-ttu-id="4e906-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4e906-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e906-129">-PassThru</span></span>
<span data-ttu-id="4e906-130">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4e906-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4e906-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e906-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e906-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4e906-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4e906-133">-ResourceId</span></span>
<span data-ttu-id="4e906-134">Service Bus-Abonnement-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4e906-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="4e906-135">-Topic</span></span>
<span data-ttu-id="4e906-136">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="4e906-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e906-137">-Confirm</span></span>
<span data-ttu-id="4e906-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e906-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e906-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e906-139">-WhatIf</span></span>
<span data-ttu-id="4e906-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e906-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e906-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e906-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e906-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e906-142">CommonParameters</span></span>
<span data-ttu-id="4e906-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e906-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e906-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e906-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e906-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e906-145">INPUTS</span></span>

### <span data-ttu-id="4e906-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4e906-146">System.String</span></span>

### <span data-ttu-id="4e906-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4e906-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="4e906-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e906-148">OUTPUTS</span></span>

### <span data-ttu-id="4e906-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e906-149">System.Boolean</span></span>

## <span data-ttu-id="4e906-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e906-150">NOTES</span></span>

## <span data-ttu-id="4e906-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e906-151">RELATED LINKS</span></span>
