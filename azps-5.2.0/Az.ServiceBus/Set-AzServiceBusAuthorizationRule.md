---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357369"
---
# <span data-ttu-id="abd3f-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="abd3f-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="abd3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="abd3f-103">Aktualisiert die Beschreibung der angegebenen Autorisierungsregel für den angegebenen Namespace oder die angegebene Warteschlange oder das angegebene Thema des Service Bus.</span><span class="sxs-lookup"><span data-stu-id="abd3f-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="abd3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abd3f-104">SYNTAX</span></span>

### <span data-ttu-id="abd3f-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="abd3f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd3f-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="abd3f-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd3f-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="abd3f-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd3f-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="abd3f-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd3f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abd3f-109">DESCRIPTION</span></span>
<span data-ttu-id="abd3f-110">Das **Cmdlet "Set-AzServiceBusAuthorizationRule"** aktualisiert die Beschreibung für die angegebene Autorisierungsregel im angegebenen Namespace oder in der Warteschlange oder im angegebenen Thema des Service Bus.</span><span class="sxs-lookup"><span data-stu-id="abd3f-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="abd3f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="abd3f-111">EXAMPLES</span></span>

### <span data-ttu-id="abd3f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abd3f-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="abd3f-113">Entfernt **"Manage"** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im `SB-Example1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="abd3f-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="abd3f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="abd3f-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="abd3f-115">Entfernt **"Manage"** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in der `SBQueue` Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="abd3f-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="abd3f-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="abd3f-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="abd3f-117">Entfernt **"Manage"** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im `SBTopic` Thema.</span><span class="sxs-lookup"><span data-stu-id="abd3f-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="abd3f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abd3f-118">PARAMETERS</span></span>

### <span data-ttu-id="abd3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd3f-119">-DefaultProfile</span></span>
<span data-ttu-id="abd3f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abd3f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd3f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abd3f-121">-InputObject</span></span>
<span data-ttu-id="abd3f-122">ServiceBus AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="abd3f-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abd3f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="abd3f-123">-Name</span></span>
<span data-ttu-id="abd3f-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="abd3f-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="abd3f-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="abd3f-125">-Namespace</span></span>
<span data-ttu-id="abd3f-126">Namespacename</span><span class="sxs-lookup"><span data-stu-id="abd3f-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abd3f-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="abd3f-127">-Queue</span></span>
<span data-ttu-id="abd3f-128">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="abd3f-128">Queue Name</span></span>

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

### <span data-ttu-id="abd3f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd3f-129">-ResourceGroupName</span></span>
<span data-ttu-id="abd3f-130">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="abd3f-130">Resource Group Name</span></span>

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

### <span data-ttu-id="abd3f-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="abd3f-131">-Rights</span></span>
<span data-ttu-id="abd3f-132">Rechte, z. B. @("Zuhören";"Senden";"Verwalten")</span><span class="sxs-lookup"><span data-stu-id="abd3f-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abd3f-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="abd3f-133">-Topic</span></span>
<span data-ttu-id="abd3f-134">Themaname</span><span class="sxs-lookup"><span data-stu-id="abd3f-134">Topic Name</span></span>

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

### <span data-ttu-id="abd3f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abd3f-135">-Confirm</span></span>
<span data-ttu-id="abd3f-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abd3f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd3f-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="abd3f-137">-WhatIf</span></span>
<span data-ttu-id="abd3f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abd3f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd3f-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abd3f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd3f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd3f-140">CommonParameters</span></span>
<span data-ttu-id="abd3f-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd3f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd3f-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd3f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd3f-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="abd3f-143">INPUTS</span></span>

### <span data-ttu-id="abd3f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="abd3f-144">System.String</span></span>

### <span data-ttu-id="abd3f-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="abd3f-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="abd3f-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="abd3f-146">System.String[]</span></span>

## <span data-ttu-id="abd3f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="abd3f-147">OUTPUTS</span></span>

### <span data-ttu-id="abd3f-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="abd3f-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="abd3f-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="abd3f-149">NOTES</span></span>

## <span data-ttu-id="abd3f-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="abd3f-150">RELATED LINKS</span></span>
