---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505013"
---
# <span data-ttu-id="8f9b3-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f9b3-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="8f9b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9b3-103">Erstellt eine neue Autorisierungsregel für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f9b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f9b3-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8f9b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f9b3-105">DESCRIPTION</span></span>
<span data-ttu-id="8f9b3-106">Das New-AzureRmEventHubNamespaceAuthorizationRule-Cmdlet erstellt eine neue Autorisierungsregel für den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="8f9b3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f9b3-107">EXAMPLES</span></span>

### <span data-ttu-id="8f9b3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f9b3-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="8f9b3-109">Erstellt die Autorisierungsregel \` MyAuthRuleName \` mit Listen-und sende rechten für Event Hubs-Namespace \` mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8f9b3-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8f9b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f9b3-110">PARAMETERS</span></span>

### <span data-ttu-id="8f9b3-111">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="8f9b3-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="8f9b3-112">Name der Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="8f9b3-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="8f9b3-113">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="8f9b3-113">-NamespaceName</span></span>
<span data-ttu-id="8f9b3-114">Der Namespacename des Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="8f9b3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f9b3-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f9b3-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-116">Resource group name.</span></span>

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

### <span data-ttu-id="8f9b3-117">-Rechte</span><span class="sxs-lookup"><span data-stu-id="8f9b3-117">-Rights</span></span>
<span data-ttu-id="8f9b3-118">Rechte; Beispiel: @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="8f9b3-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f9b3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f9b3-119">-Confirm</span></span>
<span data-ttu-id="8f9b3-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f9b3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f9b3-121">-WhatIf</span></span>
<span data-ttu-id="8f9b3-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f9b3-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f9b3-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="8f9b3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f9b3-124">INPUTS</span></span>

### <span data-ttu-id="8f9b3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8f9b3-125">System.String</span></span>

## <span data-ttu-id="8f9b3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f9b3-126">OUTPUTS</span></span>

### <span data-ttu-id="8f9b3-127">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8f9b3-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8f9b3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f9b3-128">NOTES</span></span>

## <span data-ttu-id="8f9b3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f9b3-129">RELATED LINKS</span></span>

