---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939936"
---
# <span data-ttu-id="6008a-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="6008a-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="6008a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6008a-102">SYNOPSIS</span></span>
<span data-ttu-id="6008a-103">Entfernt das Abonnement für ein Thema aus dem angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6008a-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6008a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6008a-104">SYNTAX</span></span>

### <span data-ttu-id="6008a-105">SubscriptionPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6008a-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6008a-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6008a-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6008a-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6008a-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6008a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6008a-108">DESCRIPTION</span></span>
<span data-ttu-id="6008a-109">Das **Cmdlet Remove-AzServiceBusSubscription** entfernt das Abonnement für ein Thema aus dem angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6008a-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6008a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6008a-110">EXAMPLES</span></span>

### <span data-ttu-id="6008a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6008a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="6008a-112">Entfernt das Abonnement `SB-TopicSubscription-Example1` für das Thema im `SB-Topic_exampl1` angegebenen Service Bus-Namespace. `SB-Example1`</span><span class="sxs-lookup"><span data-stu-id="6008a-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6008a-113">Beispiel 2: InputObject – Verwenden von Variablen:</span><span class="sxs-lookup"><span data-stu-id="6008a-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="6008a-114">Beispiel 3: InputObject – Verwenden von Piping:</span><span class="sxs-lookup"><span data-stu-id="6008a-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="6008a-115">Beispiel 4: ResourceId – Verwenden von Variablen:</span><span class="sxs-lookup"><span data-stu-id="6008a-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="6008a-116">Beispiel 5: ResourceId – Verwenden des Zeichenfolgenwerts:</span><span class="sxs-lookup"><span data-stu-id="6008a-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="6008a-117">Entfernt das Abonnement, das über die ARM id in $resourceid/string für den Parameter -ResourceId bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6008a-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="6008a-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6008a-118">PARAMETERS</span></span>

### <span data-ttu-id="6008a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6008a-119">-AsJob</span></span>
<span data-ttu-id="6008a-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6008a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6008a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6008a-121">-DefaultProfile</span></span>
<span data-ttu-id="6008a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6008a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6008a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6008a-123">-InputObject</span></span>
<span data-ttu-id="6008a-124">Service Bus Subscription Object</span><span class="sxs-lookup"><span data-stu-id="6008a-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="6008a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6008a-125">-Name</span></span>
<span data-ttu-id="6008a-126">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="6008a-126">Subscription Name</span></span>

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

### <span data-ttu-id="6008a-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6008a-127">-Namespace</span></span>
<span data-ttu-id="6008a-128">Namespacename</span><span class="sxs-lookup"><span data-stu-id="6008a-128">Namespace Name</span></span>

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

### <span data-ttu-id="6008a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6008a-129">-PassThru</span></span>
<span data-ttu-id="6008a-130">Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="6008a-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6008a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6008a-131">-ResourceGroupName</span></span>
<span data-ttu-id="6008a-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6008a-132">The name of the resource group</span></span>

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

### <span data-ttu-id="6008a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6008a-133">-ResourceId</span></span>
<span data-ttu-id="6008a-134">Ressourcen-ID des Dienstbusabonnements</span><span class="sxs-lookup"><span data-stu-id="6008a-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="6008a-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="6008a-135">-Topic</span></span>
<span data-ttu-id="6008a-136">Topic Name</span><span class="sxs-lookup"><span data-stu-id="6008a-136">Topic Name</span></span>

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

### <span data-ttu-id="6008a-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6008a-137">-Confirm</span></span>
<span data-ttu-id="6008a-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6008a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6008a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6008a-139">-WhatIf</span></span>
<span data-ttu-id="6008a-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6008a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6008a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6008a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6008a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6008a-142">CommonParameters</span></span>
<span data-ttu-id="6008a-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6008a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6008a-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6008a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6008a-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6008a-145">INPUTS</span></span>

### <span data-ttu-id="6008a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6008a-146">System.String</span></span>

### <span data-ttu-id="6008a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="6008a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="6008a-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6008a-148">OUTPUTS</span></span>

### <span data-ttu-id="6008a-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6008a-149">System.Boolean</span></span>

## <span data-ttu-id="6008a-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6008a-150">NOTES</span></span>

## <span data-ttu-id="6008a-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6008a-151">RELATED LINKS</span></span>
