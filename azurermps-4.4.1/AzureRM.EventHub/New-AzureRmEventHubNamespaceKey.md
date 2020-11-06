---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505009"
---
# <span data-ttu-id="2dd21-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="2dd21-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="2dd21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dd21-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd21-103">Erstellt einen neuen primären oder sekundären Schlüssel für die Autorisierungsregel für den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2dd21-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dd21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dd21-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2dd21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dd21-105">DESCRIPTION</span></span>
<span data-ttu-id="2dd21-106">Das New-AzureRmEventHubNamespaceKey-Cmdlet generiert den primären oder sekundären Schlüssel für die angegebene Autorisierungsregel für den angegebenen Event Hubs-Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="2dd21-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="2dd21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dd21-107">EXAMPLES</span></span>

### <span data-ttu-id="2dd21-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2dd21-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="2dd21-109">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` im Event Hubs \` -Namespace mynamespacename \` mit Ressourcengruppen- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2dd21-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2dd21-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dd21-110">PARAMETERS</span></span>

### <span data-ttu-id="2dd21-111">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="2dd21-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="2dd21-112">Name der Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="2dd21-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="2dd21-113">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="2dd21-113">-NamespaceName</span></span>
<span data-ttu-id="2dd21-114">Der Namespacename des Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="2dd21-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="2dd21-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="2dd21-115">-RegenerateKeys</span></span>
<span data-ttu-id="2dd21-116">Schlüssel zum Regenerieren: \` Primärschlüssel \` oder \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="2dd21-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd21-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2dd21-117">-ResourceGroup</span></span>
<span data-ttu-id="2dd21-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2dd21-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2dd21-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2dd21-119">-Confirm</span></span>
<span data-ttu-id="2dd21-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dd21-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd21-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd21-121">-WhatIf</span></span>
<span data-ttu-id="2dd21-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dd21-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd21-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dd21-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2dd21-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dd21-124">INPUTS</span></span>

### <span data-ttu-id="2dd21-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2dd21-125">System.String</span></span>

## <span data-ttu-id="2dd21-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dd21-126">OUTPUTS</span></span>

### <span data-ttu-id="2dd21-127">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2dd21-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="2dd21-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dd21-128">NOTES</span></span>

## <span data-ttu-id="2dd21-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dd21-129">RELATED LINKS</span></span>

