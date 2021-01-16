---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294052"
---
# <span data-ttu-id="33a37-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="33a37-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="33a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a37-102">SYNOPSIS</span></span>
<span data-ttu-id="33a37-103">Entfernt die angegebene Regel eines bestimmten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="33a37-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="33a37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33a37-104">SYNTAX</span></span>

### <span data-ttu-id="33a37-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="33a37-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a37-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33a37-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33a37-107">DESCRIPTION</span></span>
<span data-ttu-id="33a37-108">Das **Cmdlet "Remove-AzServiceBusRule"** entfernt die Regel eines Abonnements eines bestimmten Themas.</span><span class="sxs-lookup"><span data-stu-id="33a37-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="33a37-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="33a37-109">EXAMPLES</span></span>

### <span data-ttu-id="33a37-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33a37-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="33a37-111">Entfernt die `SBRule` Abonnementregel des `SBSubscription` angegebenen `SBTopic` Themas.</span><span class="sxs-lookup"><span data-stu-id="33a37-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="33a37-112">Beispiel 2: InputObject – Verwenden der Variable:</span><span class="sxs-lookup"><span data-stu-id="33a37-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="33a37-113">Entfernt die Regel, die über den $inputobject "-InputObject"-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33a37-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="33a37-114">Beispiel 3: InputObject – Verwenden der Piping:</span><span class="sxs-lookup"><span data-stu-id="33a37-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="33a37-115">Beispiel 4: ResourceId – Verwenden einer Variablen</span><span class="sxs-lookup"><span data-stu-id="33a37-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="33a37-116">Beispiel 5: ResourceId – Verwenden des Zeichenfolgenwerts</span><span class="sxs-lookup"><span data-stu-id="33a37-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="33a37-117">Entfernt die Regel, die über die ARM"-ID in $resourceid/String für den Parameter "-ResourceId" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33a37-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="33a37-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33a37-118">PARAMETERS</span></span>

### <span data-ttu-id="33a37-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33a37-119">-AsJob</span></span>
<span data-ttu-id="33a37-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="33a37-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33a37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a37-121">-DefaultProfile</span></span>
<span data-ttu-id="33a37-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33a37-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a37-123">-Force</span><span class="sxs-lookup"><span data-stu-id="33a37-123">-Force</span></span>
<span data-ttu-id="33a37-124">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="33a37-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="33a37-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33a37-125">-InputObject</span></span>
<span data-ttu-id="33a37-126">Service Bus Rule Object</span><span class="sxs-lookup"><span data-stu-id="33a37-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="33a37-127">-Name</span><span class="sxs-lookup"><span data-stu-id="33a37-127">-Name</span></span>
<span data-ttu-id="33a37-128">Regelname</span><span class="sxs-lookup"><span data-stu-id="33a37-128">Rule Name</span></span>

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

### <span data-ttu-id="33a37-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33a37-129">-Namespace</span></span>
<span data-ttu-id="33a37-130">Namespacename</span><span class="sxs-lookup"><span data-stu-id="33a37-130">Namespace Name</span></span>

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

### <span data-ttu-id="33a37-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33a37-131">-PassThru</span></span>
<span data-ttu-id="33a37-132">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="33a37-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="33a37-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a37-133">-ResourceGroupName</span></span>
<span data-ttu-id="33a37-134">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="33a37-134">The name of the resource group</span></span>

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

### <span data-ttu-id="33a37-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33a37-135">-ResourceId</span></span>
<span data-ttu-id="33a37-136">Ressourcen-ID der Dienstbusregel</span><span class="sxs-lookup"><span data-stu-id="33a37-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="33a37-137">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="33a37-137">-Subscription</span></span>
<span data-ttu-id="33a37-138">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="33a37-138">Subscription Name</span></span>

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

### <span data-ttu-id="33a37-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="33a37-139">-Topic</span></span>
<span data-ttu-id="33a37-140">Themaname</span><span class="sxs-lookup"><span data-stu-id="33a37-140">Topic Name</span></span>

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

### <span data-ttu-id="33a37-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33a37-141">-Confirm</span></span>
<span data-ttu-id="33a37-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33a37-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a37-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="33a37-143">-WhatIf</span></span>
<span data-ttu-id="33a37-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33a37-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a37-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33a37-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a37-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a37-146">CommonParameters</span></span>
<span data-ttu-id="33a37-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a37-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a37-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a37-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a37-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="33a37-149">INPUTS</span></span>

### <span data-ttu-id="33a37-150">System.String</span><span class="sxs-lookup"><span data-stu-id="33a37-150">System.String</span></span>

### <span data-ttu-id="33a37-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="33a37-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="33a37-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="33a37-152">OUTPUTS</span></span>

### <span data-ttu-id="33a37-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33a37-153">System.Boolean</span></span>

## <span data-ttu-id="33a37-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="33a37-154">NOTES</span></span>

## <span data-ttu-id="33a37-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="33a37-155">RELATED LINKS</span></span>
