---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505949"
---
# <span data-ttu-id="6030c-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6030c-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="6030c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6030c-102">SYNOPSIS</span></span>
<span data-ttu-id="6030c-103">Aktualisiert die Autorisierungsregel für den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6030c-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6030c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6030c-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6030c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6030c-105">DESCRIPTION</span></span>
<span data-ttu-id="6030c-106">Das Set-AzureRmEventHubNamespaceAuthorizationRule-Cmdlet aktualisiert die Autorisierungsregel für den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6030c-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="6030c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6030c-107">EXAMPLES</span></span>

### <span data-ttu-id="6030c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6030c-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="6030c-109">Aktualisiert die Autorisierungsregel \` MyAuthRuleName \` , um die Berechtigung zum Verwalten von Berechtigungen zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="6030c-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="6030c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6030c-110">PARAMETERS</span></span>

### <span data-ttu-id="6030c-111">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="6030c-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="6030c-112">Der Name der Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="6030c-112">The authorization rule name.</span></span>
<span data-ttu-id="6030c-113">Erforderlich, wenn-AuthruleObj nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6030c-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6030c-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="6030c-114">-AuthRuleObj</span></span>
<span data-ttu-id="6030c-115">Das Event Hubs-Namespace Autorisierungsregel Objekt.</span><span class="sxs-lookup"><span data-stu-id="6030c-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6030c-116">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="6030c-116">-NamespaceName</span></span>
<span data-ttu-id="6030c-117">Der Namespacename des Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="6030c-117">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6030c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6030c-118">-ResourceGroupName</span></span>
<span data-ttu-id="6030c-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6030c-119">Resource group name.</span></span>

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

### <span data-ttu-id="6030c-120">-Rechte</span><span class="sxs-lookup"><span data-stu-id="6030c-120">-Rights</span></span>
<span data-ttu-id="6030c-121">Erforderlich, wenn-AuthruleObj nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6030c-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="6030c-122">Rechte Beispiel: @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="6030c-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6030c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6030c-123">-Confirm</span></span>
<span data-ttu-id="6030c-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6030c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6030c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6030c-125">-WhatIf</span></span>
<span data-ttu-id="6030c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6030c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6030c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6030c-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="6030c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6030c-128">INPUTS</span></span>

### <span data-ttu-id="6030c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6030c-129">System.String</span></span>

## <span data-ttu-id="6030c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6030c-130">OUTPUTS</span></span>

### <span data-ttu-id="6030c-131">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6030c-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6030c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="6030c-132">NOTES</span></span>

## <span data-ttu-id="6030c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6030c-133">RELATED LINKS</span></span>

