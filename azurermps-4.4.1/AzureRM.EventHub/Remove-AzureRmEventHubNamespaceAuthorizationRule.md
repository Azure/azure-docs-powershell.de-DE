---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663326"
---
# <span data-ttu-id="1ed8c-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ed8c-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="1ed8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ed8c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed8c-103">Löscht die angegebene Autorisierungsregel für den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed8c-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1ed8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ed8c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed8c-106">Das Remove-AzureRmEventHubNamespaceAuthorizationRule-Cmdlet entfernt und löscht die angegebene Autorisierungsregel für den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="1ed8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ed8c-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed8c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ed8c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="1ed8c-109">Entfernt die Autorisierungsregel \` MyAuthRuleName \` aus dem Namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1ed8c-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="1ed8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ed8c-110">PARAMETERS</span></span>

### <span data-ttu-id="1ed8c-111">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="1ed8c-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="1ed8c-112">Der Name der Namespace Autorisierungsregel für Ereignis Hubs</span><span class="sxs-lookup"><span data-stu-id="1ed8c-112">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed8c-113">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="1ed8c-113">-NamespaceName</span></span>
<span data-ttu-id="1ed8c-114">Der Namespacename des Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="1ed8c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed8c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ed8c-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-116">Resource group name.</span></span>

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

### <span data-ttu-id="1ed8c-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ed8c-117">-Confirm</span></span>
<span data-ttu-id="1ed8c-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed8c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed8c-119">-WhatIf</span></span>
<span data-ttu-id="1ed8c-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed8c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ed8c-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="1ed8c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ed8c-122">INPUTS</span></span>

### <span data-ttu-id="1ed8c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1ed8c-123">System.String</span></span>

## <span data-ttu-id="1ed8c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ed8c-124">OUTPUTS</span></span>

### <span data-ttu-id="1ed8c-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ed8c-125">System.Boolean</span></span>

## <span data-ttu-id="1ed8c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ed8c-126">NOTES</span></span>

## <span data-ttu-id="1ed8c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ed8c-127">RELATED LINKS</span></span>

