---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663583"
---
# <span data-ttu-id="224f1-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="224f1-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="224f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="224f1-102">SYNOPSIS</span></span>
<span data-ttu-id="224f1-103">Erstellt eine neue Autorisierungsregel für Ereignis Hubs für Namespace oder eventhub.</span><span class="sxs-lookup"><span data-stu-id="224f1-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="224f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="224f1-104">SYNTAX</span></span>

### <span data-ttu-id="224f1-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="224f1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="224f1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="224f1-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="224f1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="224f1-107">DESCRIPTION</span></span>
<span data-ttu-id="224f1-108">Das New-AzureRmEventHubAuthorizationRule-Cmdlet erstellt eine neue Autorisierungsregel für Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="224f1-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="224f1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="224f1-109">EXAMPLES</span></span>

### <span data-ttu-id="224f1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="224f1-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="224f1-111">Erstellt eine Autorisierungsregel \` MyAuthRuleName \` Gewährung von Listen-und sende Rechten an den Namespace \` mynamespacename \` mit Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="224f1-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="224f1-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="224f1-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="224f1-113">Erstellt eine Autorisierungsregel \` MyAuthRuleName \` Erteilen von Listen-und sende rechten für den Ereignis-Hub \` MyEventHubName \` im Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="224f1-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="224f1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="224f1-114">PARAMETERS</span></span>

### <span data-ttu-id="224f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="224f1-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="224f1-116">Resource group name.</span></span>

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

### <span data-ttu-id="224f1-117">-Rechte</span><span class="sxs-lookup"><span data-stu-id="224f1-117">-Rights</span></span>
<span data-ttu-id="224f1-118">Rechte Beispiel: @ ("Listen", "Senden", "verwalten").</span><span class="sxs-lookup"><span data-stu-id="224f1-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224f1-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="224f1-119">-Confirm</span></span>
<span data-ttu-id="224f1-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="224f1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="224f1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="224f1-121">-WhatIf</span></span>
<span data-ttu-id="224f1-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="224f1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="224f1-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="224f1-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="224f1-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="224f1-124">-EventHub</span></span>
<span data-ttu-id="224f1-125">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="224f1-125">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224f1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="224f1-126">-Name</span></span>
<span data-ttu-id="224f1-127">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="224f1-127">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224f1-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="224f1-128">-Namespace</span></span>
<span data-ttu-id="224f1-129">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="224f1-129">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="224f1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="224f1-130">INPUTS</span></span>

### <span data-ttu-id="224f1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="224f1-131">System.String</span></span>

## <span data-ttu-id="224f1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="224f1-132">OUTPUTS</span></span>

### <span data-ttu-id="224f1-133">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="224f1-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="224f1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="224f1-134">NOTES</span></span>

## <span data-ttu-id="224f1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="224f1-135">RELATED LINKS</span></span>

