---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 5a33eae7e31ecdc793411bcddc2855d0dbcce8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923435"
---
# <span data-ttu-id="ddd86-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ddd86-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ddd86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd86-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd86-103">Entfernt die Autorisierungsregel eines Service Bus-Namespaces oder einer Warteschlange oder eines Themas aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddd86-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="ddd86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddd86-104">SYNTAX</span></span>

### <span data-ttu-id="ddd86-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ddd86-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd86-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ddd86-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd86-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ddd86-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd86-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddd86-108">DESCRIPTION</span></span>
<span data-ttu-id="ddd86-109">Das **Cmdlet Remove-AzServiceBusAuthorizationRule** entfernt die Autorisierungsregel eines Service Bus-Namespaces oder einer Warteschlange oder eines Themas für die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddd86-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="ddd86-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddd86-110">EXAMPLES</span></span>

### <span data-ttu-id="ddd86-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddd86-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="ddd86-112">Entfernt die `SBAuthoRule1` Autorisierungsregel des `SB-Example1` Namespaces aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddd86-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="ddd86-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddd86-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="ddd86-114">Entfernt die Autorisierungsregel `SBAuthoRule1` der Warteschlange aus der `SBQueue` angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddd86-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="ddd86-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ddd86-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="ddd86-116">Entfernt die `SBAuthoRule1` Autorisierungsregel des Themas `SBTopic` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddd86-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="ddd86-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ddd86-117">PARAMETERS</span></span>

### <span data-ttu-id="ddd86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd86-118">-DefaultProfile</span></span>
<span data-ttu-id="ddd86-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddd86-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd86-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ddd86-120">-Force</span></span>
<span data-ttu-id="ddd86-121">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="ddd86-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ddd86-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddd86-122">-InputObject</span></span>
<span data-ttu-id="ddd86-123">ServiceBus AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="ddd86-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd86-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ddd86-124">-Name</span></span>
<span data-ttu-id="ddd86-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="ddd86-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd86-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ddd86-126">-Namespace</span></span>
<span data-ttu-id="ddd86-127">Namespacename</span><span class="sxs-lookup"><span data-stu-id="ddd86-127">Namespace Name</span></span>

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

### <span data-ttu-id="ddd86-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddd86-128">-PassThru</span></span>
<span data-ttu-id="ddd86-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ddd86-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ddd86-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ddd86-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ddd86-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="ddd86-131">-Queue</span></span>
<span data-ttu-id="ddd86-132">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="ddd86-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd86-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd86-133">-ResourceGroupName</span></span>
<span data-ttu-id="ddd86-134">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ddd86-134">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd86-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="ddd86-135">-Topic</span></span>
<span data-ttu-id="ddd86-136">Topic Name</span><span class="sxs-lookup"><span data-stu-id="ddd86-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd86-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddd86-137">-Confirm</span></span>
<span data-ttu-id="ddd86-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddd86-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd86-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd86-139">-WhatIf</span></span>
<span data-ttu-id="ddd86-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddd86-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd86-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddd86-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd86-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd86-142">CommonParameters</span></span>
<span data-ttu-id="ddd86-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd86-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd86-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd86-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd86-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddd86-145">INPUTS</span></span>

### <span data-ttu-id="ddd86-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ddd86-146">System.String</span></span>

### <span data-ttu-id="ddd86-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ddd86-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ddd86-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddd86-148">OUTPUTS</span></span>

### <span data-ttu-id="ddd86-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd86-149">System.Boolean</span></span>

## <span data-ttu-id="ddd86-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ddd86-150">NOTES</span></span>

## <span data-ttu-id="ddd86-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ddd86-151">RELATED LINKS</span></span>
