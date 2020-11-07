---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662614"
---
# <span data-ttu-id="5d262-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5d262-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="5d262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d262-102">SYNOPSIS</span></span>
<span data-ttu-id="5d262-103">Entfernt die Autorisierungsregel für einen ServiceBus-Namespace oder eine Warteschlange oder ein Thema aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d262-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d262-104">SYNTAX</span></span>

### <span data-ttu-id="5d262-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d262-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5d262-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d262-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5d262-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d262-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5d262-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d262-108">DESCRIPTION</span></span>
<span data-ttu-id="5d262-109">Das Cmdlet **Remove-AzureRmServiceBusAuthorizationRule** entfernt die Autorisierungsregel für einen ServiceBus-Namespace oder eine Warteschlange oder ein Thema für die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d262-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="5d262-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d262-110">EXAMPLES</span></span>

### <span data-ttu-id="5d262-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d262-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="5d262-112">Entfernt die Autorisierungsregel `SBAuthoRule1` für Namespace `SB-Example1` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d262-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="5d262-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d262-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="5d262-114">Entfernt die Autorisierungsregel `SBAuthoRule1` der Warteschlange `SBQueue` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d262-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="5d262-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5d262-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="5d262-116">Entfernt die Autorisierungsregel `SBAuthoRule1` des Themas `SBTopic` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d262-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="5d262-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d262-117">PARAMETERS</span></span>

### <span data-ttu-id="5d262-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d262-118">-Confirm</span></span>
<span data-ttu-id="5d262-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d262-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5d262-120">-Force</span></span>
<span data-ttu-id="5d262-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5d262-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5d262-122">-Name</span></span>
<span data-ttu-id="5d262-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="5d262-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5d262-124">-Namespace</span></span>
<span data-ttu-id="5d262-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="5d262-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d262-126">-PassThru</span></span>
<span data-ttu-id="5d262-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="5d262-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="5d262-128">-Queue</span></span>
<span data-ttu-id="5d262-129">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5d262-129">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d262-130">-ResourceGroupName</span></span>
<span data-ttu-id="5d262-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d262-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-132">-Topic</span><span class="sxs-lookup"><span data-stu-id="5d262-132">-Topic</span></span>
<span data-ttu-id="5d262-133">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="5d262-133">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d262-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d262-134">-WhatIf</span></span>
<span data-ttu-id="5d262-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d262-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d262-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d262-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5d262-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d262-137">INPUTS</span></span>

### <span data-ttu-id="5d262-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5d262-138">System.String</span></span>


## <span data-ttu-id="5d262-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d262-139">OUTPUTS</span></span>

### <span data-ttu-id="5d262-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d262-140">System.Boolean</span></span>


## <span data-ttu-id="5d262-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d262-141">NOTES</span></span>

## <span data-ttu-id="5d262-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d262-142">RELATED LINKS</span></span>

