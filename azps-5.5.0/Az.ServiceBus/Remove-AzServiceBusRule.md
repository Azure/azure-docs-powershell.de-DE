---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168857"
---
# <span data-ttu-id="463d3-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="463d3-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="463d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463d3-102">SYNOPSIS</span></span>
<span data-ttu-id="463d3-103">Entfernt die angegebene Regel eines bestimmten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="463d3-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="463d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="463d3-104">SYNTAX</span></span>

### <span data-ttu-id="463d3-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="463d3-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="463d3-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="463d3-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463d3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="463d3-107">DESCRIPTION</span></span>
<span data-ttu-id="463d3-108">Das **Cmdlet "Remove-AzServiceBusRule"** entfernt die Regel eines Abonnements eines bestimmten Themas.</span><span class="sxs-lookup"><span data-stu-id="463d3-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="463d3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="463d3-109">EXAMPLES</span></span>

### <span data-ttu-id="463d3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="463d3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="463d3-111">Entfernt die `SBRule` Abonnementregel des `SBSubscription` angegebenen `SBTopic` Themas.</span><span class="sxs-lookup"><span data-stu-id="463d3-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="463d3-112">Beispiel 2: InputObject – Verwenden der Variable:</span><span class="sxs-lookup"><span data-stu-id="463d3-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="463d3-113">Entfernt die Regel, die über den $inputobject "-InputObject"-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="463d3-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="463d3-114">Beispiel 3: InputObject – Verwenden der Piping:</span><span class="sxs-lookup"><span data-stu-id="463d3-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="463d3-115">Beispiel 4: ResourceId – Verwenden einer Variablen</span><span class="sxs-lookup"><span data-stu-id="463d3-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="463d3-116">Beispiel 5: ResourceId – Verwenden des Zeichenfolgenwerts</span><span class="sxs-lookup"><span data-stu-id="463d3-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="463d3-117">Entfernt die Regel, die über die ARM"-ID in $resourceid/String für den Parameter "-ResourceId" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="463d3-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="463d3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="463d3-118">PARAMETERS</span></span>

### <span data-ttu-id="463d3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="463d3-119">-AsJob</span></span>
<span data-ttu-id="463d3-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="463d3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="463d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463d3-121">-DefaultProfile</span></span>
<span data-ttu-id="463d3-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="463d3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463d3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="463d3-123">-Force</span></span>
<span data-ttu-id="463d3-124">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="463d3-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="463d3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="463d3-125">-InputObject</span></span>
<span data-ttu-id="463d3-126">Service Bus Rule Object</span><span class="sxs-lookup"><span data-stu-id="463d3-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="463d3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="463d3-127">-Name</span></span>
<span data-ttu-id="463d3-128">Regelname</span><span class="sxs-lookup"><span data-stu-id="463d3-128">Rule Name</span></span>

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

### <span data-ttu-id="463d3-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="463d3-129">-Namespace</span></span>
<span data-ttu-id="463d3-130">Namespacename</span><span class="sxs-lookup"><span data-stu-id="463d3-130">Namespace Name</span></span>

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

### <span data-ttu-id="463d3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="463d3-131">-PassThru</span></span>
<span data-ttu-id="463d3-132">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="463d3-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="463d3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463d3-133">-ResourceGroupName</span></span>
<span data-ttu-id="463d3-134">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="463d3-134">The name of the resource group</span></span>

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

### <span data-ttu-id="463d3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="463d3-135">-ResourceId</span></span>
<span data-ttu-id="463d3-136">Ressourcen-ID der Dienstbusregel</span><span class="sxs-lookup"><span data-stu-id="463d3-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="463d3-137">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="463d3-137">-Subscription</span></span>
<span data-ttu-id="463d3-138">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="463d3-138">Subscription Name</span></span>

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

### <span data-ttu-id="463d3-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="463d3-139">-Topic</span></span>
<span data-ttu-id="463d3-140">Themaname</span><span class="sxs-lookup"><span data-stu-id="463d3-140">Topic Name</span></span>

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

### <span data-ttu-id="463d3-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="463d3-141">-Confirm</span></span>
<span data-ttu-id="463d3-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="463d3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463d3-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="463d3-143">-WhatIf</span></span>
<span data-ttu-id="463d3-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="463d3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="463d3-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="463d3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463d3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463d3-146">CommonParameters</span></span>
<span data-ttu-id="463d3-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463d3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463d3-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463d3-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463d3-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="463d3-149">INPUTS</span></span>

### <span data-ttu-id="463d3-150">System.String</span><span class="sxs-lookup"><span data-stu-id="463d3-150">System.String</span></span>

### <span data-ttu-id="463d3-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="463d3-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="463d3-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="463d3-152">OUTPUTS</span></span>

### <span data-ttu-id="463d3-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="463d3-153">System.Boolean</span></span>

## <span data-ttu-id="463d3-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="463d3-154">NOTES</span></span>

## <span data-ttu-id="463d3-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="463d3-155">RELATED LINKS</span></span>
