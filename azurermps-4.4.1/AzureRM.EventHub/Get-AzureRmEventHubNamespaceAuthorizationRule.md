---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665062"
---
# <span data-ttu-id="faf5a-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="faf5a-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="faf5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="faf5a-103">Ruft die Details einer Eventubs-Namespace Autorisierungsregel ab oder ruft eine Liste mit Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="faf5a-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf5a-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="faf5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faf5a-105">DESCRIPTION</span></span>
<span data-ttu-id="faf5a-106">Das Get-AzureRmEventHubNamespaceAuthorizationRule-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Namespace Autorisierungsregel oder eine Liste mit Namespace Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="faf5a-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="faf5a-107">Wenn der Name der Autorisierungsregel angegeben ist, werden die Details einer einzelnen Autorisierungsregel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="faf5a-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="faf5a-108">Wenn kein Autorisierungsregel Name angegeben wird, wird eine Liste aller Autorisierungsregeln im Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="faf5a-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="faf5a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faf5a-109">EXAMPLES</span></span>

### <span data-ttu-id="faf5a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faf5a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="faf5a-111">Gibt die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` mynamespacename des Ereignis Hubs \` mit der Ressourcengruppe \` MyResourceGroupName zurück \` .</span><span class="sxs-lookup"><span data-stu-id="faf5a-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="faf5a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="faf5a-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="faf5a-113">Gibt die standardmäßige Autorisierungsregel \` RootManageSharedAccessKey \` im Namespace \` mynamespacename des Ereignis Hubs \` mit der Ressourcengruppe \` MyResourceGroupName zurück \` .</span><span class="sxs-lookup"><span data-stu-id="faf5a-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="faf5a-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="faf5a-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="faf5a-115">Gibt alle Autorisierungsregeln im Event Hubs \` -Namespace mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName zurück \` .</span><span class="sxs-lookup"><span data-stu-id="faf5a-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="faf5a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf5a-116">PARAMETERS</span></span>

### <span data-ttu-id="faf5a-117">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="faf5a-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="faf5a-118">Der Name der Namespace Autorisierungsregel für Ereignis Hubs</span><span class="sxs-lookup"><span data-stu-id="faf5a-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faf5a-119">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="faf5a-119">-NamespaceName</span></span>
<span data-ttu-id="faf5a-120">Der Namespacename des Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="faf5a-120">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="faf5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="faf5a-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="faf5a-122">Resource group name.</span></span>

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

## <span data-ttu-id="faf5a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faf5a-123">INPUTS</span></span>

### <span data-ttu-id="faf5a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="faf5a-124">System.String</span></span>

## <span data-ttu-id="faf5a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faf5a-125">OUTPUTS</span></span>

### <span data-ttu-id="faf5a-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="faf5a-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="faf5a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="faf5a-127">NOTES</span></span>

## <span data-ttu-id="faf5a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faf5a-128">RELATED LINKS</span></span>

