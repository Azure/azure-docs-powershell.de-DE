---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505002"
---
# <span data-ttu-id="8581c-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8581c-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="8581c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8581c-102">SYNOPSIS</span></span>
<span data-ttu-id="8581c-103">Entfernt die angegebene Ereignis-Hub-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="8581c-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8581c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8581c-104">SYNTAX</span></span>

### <span data-ttu-id="8581c-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8581c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8581c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8581c-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8581c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8581c-107">DESCRIPTION</span></span>
<span data-ttu-id="8581c-108">Das Remove-AzureRmEventHubAuthorizationRule-Cmdlet entfernt die angegebene Autorisierungsregel aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="8581c-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="8581c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8581c-109">EXAMPLES</span></span>

### <span data-ttu-id="8581c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8581c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="8581c-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8581c-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="8581c-112">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="8581c-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="8581c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8581c-113">PARAMETERS</span></span>

### <span data-ttu-id="8581c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8581c-114">-ResourceGroupName</span></span>
<span data-ttu-id="8581c-115">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8581c-115">Resource group name.</span></span>

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

### <span data-ttu-id="8581c-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8581c-116">-Confirm</span></span>
<span data-ttu-id="8581c-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8581c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8581c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8581c-118">-WhatIf</span></span>
<span data-ttu-id="8581c-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8581c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8581c-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8581c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8581c-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8581c-121">-EventHub</span></span>
<span data-ttu-id="8581c-122">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="8581c-122">EventHub Name.</span></span>

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

### <span data-ttu-id="8581c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8581c-123">-Force</span></span>
<span data-ttu-id="8581c-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8581c-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8581c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8581c-125">-Name</span></span>
<span data-ttu-id="8581c-126">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="8581c-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="8581c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8581c-127">-Namespace</span></span>
<span data-ttu-id="8581c-128">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8581c-128">Namespace Name.</span></span>

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

### <span data-ttu-id="8581c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8581c-129">-PassThru</span></span>
<span data-ttu-id="8581c-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="8581c-130">{{Fill PassThru Description}}</span></span>

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

## <span data-ttu-id="8581c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8581c-131">INPUTS</span></span>

### <span data-ttu-id="8581c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8581c-132">System.String</span></span>

## <span data-ttu-id="8581c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8581c-133">OUTPUTS</span></span>

### <span data-ttu-id="8581c-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8581c-134">System.Boolean</span></span>

## <span data-ttu-id="8581c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8581c-135">NOTES</span></span>

## <span data-ttu-id="8581c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8581c-136">RELATED LINKS</span></span>

