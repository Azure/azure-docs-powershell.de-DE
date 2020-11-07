---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: e9bb71d58627035d023b6fdc18fe4e515e728a7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823235"
---
# <span data-ttu-id="2f6db-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="2f6db-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="2f6db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f6db-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6db-103">Entfernt die angegebene Regel eines angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2f6db-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="2f6db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f6db-104">SYNTAX</span></span>

### <span data-ttu-id="2f6db-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f6db-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6db-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2f6db-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f6db-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f6db-107">DESCRIPTION</span></span>
<span data-ttu-id="2f6db-108">Das Cmdlet **Remove-AzServiceBusRule** entfernt die Regel eines Abonnements eines angegebenen Themas.</span><span class="sxs-lookup"><span data-stu-id="2f6db-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="2f6db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f6db-109">EXAMPLES</span></span>

### <span data-ttu-id="2f6db-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f6db-110">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="2f6db-111">Entfernt die `SBRule` Abonnementregel `SBSubscription` des angegebenen Themas `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="2f6db-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="2f6db-112">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="2f6db-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="2f6db-113">Entfernt die Regel, die über $Inputobject for-Inputobject-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2f6db-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="2f6db-114">Beispiel 2,2-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="2f6db-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="2f6db-115">Beispiel 3,1-Resourcen-using-Variable</span><span class="sxs-lookup"><span data-stu-id="2f6db-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="2f6db-116">Beispiel 3,1-resourcecode mit Zeichenfolgenwert</span><span class="sxs-lookup"><span data-stu-id="2f6db-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="2f6db-117">Entfernt die Regel, die über die Arm-ID bereitgestellt wird, in $ResourceId/String for-Resourcen-Parameter</span><span class="sxs-lookup"><span data-stu-id="2f6db-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="2f6db-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f6db-118">PARAMETERS</span></span>

### <span data-ttu-id="2f6db-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f6db-119">-AsJob</span></span>
<span data-ttu-id="2f6db-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2f6db-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f6db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6db-121">-DefaultProfile</span></span>
<span data-ttu-id="2f6db-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f6db-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f6db-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2f6db-123">-Force</span></span>
<span data-ttu-id="2f6db-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2f6db-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2f6db-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f6db-125">-InputObject</span></span>
<span data-ttu-id="2f6db-126">ServiceBus-Regelobjekt</span><span class="sxs-lookup"><span data-stu-id="2f6db-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2f6db-127">-Name</span></span>
<span data-ttu-id="2f6db-128">Regelname</span><span class="sxs-lookup"><span data-stu-id="2f6db-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f6db-129">-Namespace</span></span>
<span data-ttu-id="2f6db-130">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2f6db-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f6db-131">-PassThru</span></span>
<span data-ttu-id="2f6db-132">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2f6db-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2f6db-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f6db-133">-ResourceGroupName</span></span>
<span data-ttu-id="2f6db-134">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2f6db-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2f6db-135">-ResourceId</span></span>
<span data-ttu-id="2f6db-136">Service Bus-Regel-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2f6db-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-137">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="2f6db-137">-Subscription</span></span>
<span data-ttu-id="2f6db-138">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="2f6db-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="2f6db-139">-Topic</span></span>
<span data-ttu-id="2f6db-140">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="2f6db-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6db-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f6db-141">-Confirm</span></span>
<span data-ttu-id="2f6db-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f6db-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f6db-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f6db-143">-WhatIf</span></span>
<span data-ttu-id="2f6db-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f6db-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f6db-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f6db-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f6db-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6db-146">CommonParameters</span></span>
<span data-ttu-id="2f6db-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f6db-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6db-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f6db-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6db-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f6db-149">INPUTS</span></span>

### <span data-ttu-id="2f6db-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2f6db-150">System.String</span></span>

### <span data-ttu-id="2f6db-151">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2f6db-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2f6db-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f6db-152">OUTPUTS</span></span>

### <span data-ttu-id="2f6db-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f6db-153">System.Boolean</span></span>

## <span data-ttu-id="2f6db-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f6db-154">NOTES</span></span>

## <span data-ttu-id="2f6db-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f6db-155">RELATED LINKS</span></span>
