---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505037"
---
# <span data-ttu-id="dc9d8-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dc9d8-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="dc9d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9d8-103">Ruft die Details einer Autorisierungsregel ab oder ruft eine Liste mit Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc9d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc9d8-104">SYNTAX</span></span>

### <span data-ttu-id="dc9d8-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc9d8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="dc9d8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc9d8-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="dc9d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc9d8-107">DESCRIPTION</span></span>
<span data-ttu-id="dc9d8-108">Das Get-AzureRmEventHubAuthorizationRule-Cmdlet ruft entweder die Details einer Autorisierungsregel oder eine Liste aller Autorisierungsregeln für einen angegebenen Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="dc9d8-109">Wenn der Name einer Autorisierungsregel angegeben wird, werden die Details dieser einzelnen Autorisierungsregel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="dc9d8-110">Wenn der Name einer Autorisierungsregel nicht angegeben wird, wird eine Liste aller Autorisierungsregeln für den angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="dc9d8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc9d8-111">EXAMPLES</span></span>

### <span data-ttu-id="dc9d8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc9d8-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="dc9d8-113">Ruft die Autorisierungsregel \` MyAuthRuleName \` in der Ereignis \` -Hub-MyEventHubName ab \` , die durch den Namespace \` mynamespacename beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="dc9d8-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="dc9d8-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc9d8-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="dc9d8-115">Ruft eine Liste aller Autorisierungsregeln im Ereignis-Hub \` -MyEventHubName ab \` , die durch den Namespace \` mynamespacename beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="dc9d8-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="dc9d8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc9d8-116">PARAMETERS</span></span>

### <span data-ttu-id="dc9d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc9d8-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-118">Resource group name.</span></span>

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

### <span data-ttu-id="dc9d8-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="dc9d8-119">-Eventhub</span></span>
<span data-ttu-id="dc9d8-120">Eventhub-Name.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="dc9d8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dc9d8-121">-Name</span></span>
<span data-ttu-id="dc9d8-122">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9d8-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc9d8-123">-Namespace</span></span>
<span data-ttu-id="dc9d8-124">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="dc9d8-124">Namespace Name.</span></span>

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

## <span data-ttu-id="dc9d8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc9d8-125">INPUTS</span></span>

### <span data-ttu-id="dc9d8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dc9d8-126">System.String</span></span>

## <span data-ttu-id="dc9d8-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc9d8-127">OUTPUTS</span></span>

### <span data-ttu-id="dc9d8-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dc9d8-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc9d8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc9d8-129">NOTES</span></span>

## <span data-ttu-id="dc9d8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc9d8-130">RELATED LINKS</span></span>

