---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950563"
---
# <span data-ttu-id="e4b79-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="e4b79-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="e4b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4b79-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b79-103">Entfernt die angegebene Regel eines bestimmten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="e4b79-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="e4b79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4b79-104">SYNTAX</span></span>

### <span data-ttu-id="e4b79-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4b79-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4b79-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e4b79-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b79-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4b79-107">DESCRIPTION</span></span>
<span data-ttu-id="e4b79-108">Das **Cmdlet Remove-AzServiceBusRule** entfernt die Regel eines Abonnements eines bestimmten Themas.</span><span class="sxs-lookup"><span data-stu-id="e4b79-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="e4b79-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4b79-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b79-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4b79-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="e4b79-111">Entfernt die Abonnementregel `SBRule` des `SBSubscription` angegebenen `SBTopic` Themas.</span><span class="sxs-lookup"><span data-stu-id="e4b79-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="e4b79-112">Beispiel 2: InputObject – Verwenden von Variablen:</span><span class="sxs-lookup"><span data-stu-id="e4b79-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="e4b79-113">Entfernt die über den Parameter $inputobject -InputObject bereitgestellte Regel.</span><span class="sxs-lookup"><span data-stu-id="e4b79-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="e4b79-114">Beispiel 3: InputObject – Verwenden von Piping:</span><span class="sxs-lookup"><span data-stu-id="e4b79-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="e4b79-115">Beispiel 4: ResourceId – Verwenden von Variablen</span><span class="sxs-lookup"><span data-stu-id="e4b79-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="e4b79-116">Beispiel 5: ResourceId – Verwenden des Zeichenfolgenwerts</span><span class="sxs-lookup"><span data-stu-id="e4b79-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="e4b79-117">Entfernt die Regel, die über die ARM-ID in $resourceid/Zeichenfolge für den -ResourceId-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4b79-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="e4b79-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4b79-118">PARAMETERS</span></span>

### <span data-ttu-id="e4b79-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4b79-119">-AsJob</span></span>
<span data-ttu-id="e4b79-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e4b79-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4b79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b79-121">-DefaultProfile</span></span>
<span data-ttu-id="e4b79-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4b79-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4b79-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e4b79-123">-Force</span></span>
<span data-ttu-id="e4b79-124">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="e4b79-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e4b79-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4b79-125">-InputObject</span></span>
<span data-ttu-id="e4b79-126">Dienstbusregelobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b79-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="e4b79-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e4b79-127">-Name</span></span>
<span data-ttu-id="e4b79-128">Regelname</span><span class="sxs-lookup"><span data-stu-id="e4b79-128">Rule Name</span></span>

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

### <span data-ttu-id="e4b79-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4b79-129">-Namespace</span></span>
<span data-ttu-id="e4b79-130">Namespacename</span><span class="sxs-lookup"><span data-stu-id="e4b79-130">Namespace Name</span></span>

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

### <span data-ttu-id="e4b79-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4b79-131">-PassThru</span></span>
<span data-ttu-id="e4b79-132">Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="e4b79-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e4b79-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b79-133">-ResourceGroupName</span></span>
<span data-ttu-id="e4b79-134">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e4b79-134">The name of the resource group</span></span>

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

### <span data-ttu-id="e4b79-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4b79-135">-ResourceId</span></span>
<span data-ttu-id="e4b79-136">Ressourcen-ID der Dienstbusregel</span><span class="sxs-lookup"><span data-stu-id="e4b79-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="e4b79-137">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="e4b79-137">-Subscription</span></span>
<span data-ttu-id="e4b79-138">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="e4b79-138">Subscription Name</span></span>

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

### <span data-ttu-id="e4b79-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="e4b79-139">-Topic</span></span>
<span data-ttu-id="e4b79-140">Topic Name</span><span class="sxs-lookup"><span data-stu-id="e4b79-140">Topic Name</span></span>

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

### <span data-ttu-id="e4b79-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4b79-141">-Confirm</span></span>
<span data-ttu-id="e4b79-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4b79-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b79-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b79-143">-WhatIf</span></span>
<span data-ttu-id="e4b79-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4b79-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b79-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4b79-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b79-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b79-146">CommonParameters</span></span>
<span data-ttu-id="e4b79-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b79-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b79-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b79-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b79-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4b79-149">INPUTS</span></span>

### <span data-ttu-id="e4b79-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e4b79-150">System.String</span></span>

### <span data-ttu-id="e4b79-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="e4b79-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e4b79-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4b79-152">OUTPUTS</span></span>

### <span data-ttu-id="e4b79-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4b79-153">System.Boolean</span></span>

## <span data-ttu-id="e4b79-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e4b79-154">NOTES</span></span>

## <span data-ttu-id="e4b79-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e4b79-155">RELATED LINKS</span></span>
