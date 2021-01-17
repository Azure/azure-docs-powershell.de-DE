---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361904"
---
# <span data-ttu-id="59c1a-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59c1a-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="59c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="59c1a-103">Entfernt die Autorisierungsregel eines Service Bus-Namespaces, einer Warteschlange oder eines Themas aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59c1a-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="59c1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59c1a-104">SYNTAX</span></span>

### <span data-ttu-id="59c1a-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59c1a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c1a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1a-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c1a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1a-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c1a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="59c1a-109">Das **Cmdlet "Remove-AzServiceBusAuthorizationRule"** entfernt die Autorisierungsregel eines Service Bus-Namespaces, einer Warteschlange oder eines Themas für die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59c1a-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="59c1a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59c1a-110">EXAMPLES</span></span>

### <span data-ttu-id="59c1a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59c1a-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="59c1a-112">Entfernt die `SBAuthoRule1` Autorisierungsregel für den Namespace aus der `SB-Example1` angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59c1a-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="59c1a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="59c1a-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="59c1a-114">Entfernt die Autorisierungsregel `SBAuthoRule1` der Warteschlange aus der `SBQueue` angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59c1a-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="59c1a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="59c1a-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="59c1a-116">Entfernt die Autorisierungsregel `SBAuthoRule1` des Themas `SBTopic` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59c1a-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="59c1a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59c1a-117">PARAMETERS</span></span>

### <span data-ttu-id="59c1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c1a-118">-DefaultProfile</span></span>
<span data-ttu-id="59c1a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59c1a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c1a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="59c1a-120">-Force</span></span>
<span data-ttu-id="59c1a-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="59c1a-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59c1a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c1a-122">-InputObject</span></span>
<span data-ttu-id="59c1a-123">ServiceBus AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="59c1a-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="59c1a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="59c1a-124">-Name</span></span>
<span data-ttu-id="59c1a-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="59c1a-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="59c1a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="59c1a-126">-Namespace</span></span>
<span data-ttu-id="59c1a-127">Namespacename</span><span class="sxs-lookup"><span data-stu-id="59c1a-127">Namespace Name</span></span>

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

### <span data-ttu-id="59c1a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59c1a-128">-PassThru</span></span>
<span data-ttu-id="59c1a-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="59c1a-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59c1a-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="59c1a-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59c1a-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="59c1a-131">-Queue</span></span>
<span data-ttu-id="59c1a-132">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="59c1a-132">Queue Name</span></span>

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

### <span data-ttu-id="59c1a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c1a-133">-ResourceGroupName</span></span>
<span data-ttu-id="59c1a-134">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="59c1a-134">Resource Group Name</span></span>

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

### <span data-ttu-id="59c1a-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="59c1a-135">-Topic</span></span>
<span data-ttu-id="59c1a-136">Themaname</span><span class="sxs-lookup"><span data-stu-id="59c1a-136">Topic Name</span></span>

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

### <span data-ttu-id="59c1a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59c1a-137">-Confirm</span></span>
<span data-ttu-id="59c1a-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59c1a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59c1a-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="59c1a-139">-WhatIf</span></span>
<span data-ttu-id="59c1a-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59c1a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c1a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59c1a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59c1a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c1a-142">CommonParameters</span></span>
<span data-ttu-id="59c1a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c1a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c1a-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59c1a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c1a-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59c1a-145">INPUTS</span></span>

### <span data-ttu-id="59c1a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="59c1a-146">System.String</span></span>

### <span data-ttu-id="59c1a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="59c1a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="59c1a-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59c1a-148">OUTPUTS</span></span>

### <span data-ttu-id="59c1a-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59c1a-149">System.Boolean</span></span>

## <span data-ttu-id="59c1a-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59c1a-150">NOTES</span></span>

## <span data-ttu-id="59c1a-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59c1a-151">RELATED LINKS</span></span>
