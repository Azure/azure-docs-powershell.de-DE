---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500041"
---
# <span data-ttu-id="aeec2-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aeec2-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="aeec2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aeec2-102">SYNOPSIS</span></span>
<span data-ttu-id="aeec2-103">Aktualisiert die angegebene Autorisierungsregel in einem Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="aeec2-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeec2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeec2-104">SYNTAX</span></span>

### <span data-ttu-id="aeec2-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aeec2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aeec2-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aeec2-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aeec2-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aeec2-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aeec2-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="aeec2-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="aeec2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aeec2-109">DESCRIPTION</span></span>
<span data-ttu-id="aeec2-110">Das Set-AzureRmEventHubAuthorizationRule-Cmdlet aktualisiert die angegebene Autorisierungsregel für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="aeec2-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="aeec2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeec2-111">EXAMPLES</span></span>

### <span data-ttu-id="aeec2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aeec2-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="aeec2-113">Aktualisiert die Autorisierungsregel \` MyAuthRuleName \` so, dass dem Ereignis-Hub \` \` -MyEventHubName, der vom Namespace mynamespacename zugewiesen wird, Verwaltungsrechte gewährt werden \` \` .</span><span class="sxs-lookup"><span data-stu-id="aeec2-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="aeec2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeec2-114">PARAMETERS</span></span>

### <span data-ttu-id="aeec2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeec2-115">-ResourceGroupName</span></span>
<span data-ttu-id="aeec2-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aeec2-116">Resource group name.</span></span>

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

### <span data-ttu-id="aeec2-117">-Rechte</span><span class="sxs-lookup"><span data-stu-id="aeec2-117">-Rights</span></span>
<span data-ttu-id="aeec2-118">Erforderlich, wenn "AuthruleObj" nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="aeec2-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="aeec2-119">Rechte Beispiel: @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="aeec2-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeec2-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aeec2-120">-Confirm</span></span>
<span data-ttu-id="aeec2-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aeec2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeec2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeec2-122">-WhatIf</span></span>
<span data-ttu-id="aeec2-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aeec2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeec2-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aeec2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeec2-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="aeec2-125">-EventHub</span></span>
<span data-ttu-id="aeec2-126">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="aeec2-126">EventHub Name.</span></span>

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

### <span data-ttu-id="aeec2-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aeec2-127">-InputObject</span></span>
<span data-ttu-id="aeec2-128">{{Fill Inputobject Description}}</span><span class="sxs-lookup"><span data-stu-id="aeec2-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeec2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="aeec2-129">-Name</span></span>
<span data-ttu-id="aeec2-130">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="aeec2-130">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="aeec2-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aeec2-131">-Namespace</span></span>
<span data-ttu-id="aeec2-132">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="aeec2-132">Namespace Name.</span></span>

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

## <span data-ttu-id="aeec2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aeec2-133">INPUTS</span></span>

### <span data-ttu-id="aeec2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aeec2-134">System.String</span></span>

## <span data-ttu-id="aeec2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aeec2-135">OUTPUTS</span></span>

### <span data-ttu-id="aeec2-136">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="aeec2-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="aeec2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="aeec2-137">NOTES</span></span>

## <span data-ttu-id="aeec2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aeec2-138">RELATED LINKS</span></span>

