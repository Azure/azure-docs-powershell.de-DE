---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505030"
---
# <span data-ttu-id="934d5-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="934d5-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="934d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="934d5-102">SYNOPSIS</span></span>
<span data-ttu-id="934d5-103">Ruft die Primärschlüssel Details der angegebenen Event Hubs-Autorisierungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="934d5-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="934d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="934d5-104">SYNTAX</span></span>

### <span data-ttu-id="934d5-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="934d5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="934d5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="934d5-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="934d5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="934d5-107">DESCRIPTION</span></span>
<span data-ttu-id="934d5-108">Das Get-AzureRmEventHubKey-Cmdlet gibt die primären und sekundären connectionStrings-und Schlüssel Details der angegebenen Event Hubs-Autorisierungsregel zurück.</span><span class="sxs-lookup"><span data-stu-id="934d5-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="934d5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="934d5-109">EXAMPLES</span></span>

### <span data-ttu-id="934d5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="934d5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="934d5-111">Ruft Details der primären und sekundären connectionStrings und Schlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="934d5-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="934d5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="934d5-112">PARAMETERS</span></span>

### <span data-ttu-id="934d5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="934d5-113">-ResourceGroupName</span></span>
<span data-ttu-id="934d5-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="934d5-114">Resource group name.</span></span>

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

### <span data-ttu-id="934d5-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="934d5-115">-EventHub</span></span>
<span data-ttu-id="934d5-116">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="934d5-116">EventHub Name.</span></span>

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

### <span data-ttu-id="934d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="934d5-117">-Name</span></span>
<span data-ttu-id="934d5-118">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="934d5-118">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="934d5-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="934d5-119">-Namespace</span></span>
<span data-ttu-id="934d5-120">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="934d5-120">Namespace Name.</span></span>

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

## <span data-ttu-id="934d5-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="934d5-121">INPUTS</span></span>

### <span data-ttu-id="934d5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="934d5-122">System.String</span></span>

## <span data-ttu-id="934d5-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="934d5-123">OUTPUTS</span></span>

### <span data-ttu-id="934d5-124">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="934d5-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="934d5-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="934d5-125">NOTES</span></span>

## <span data-ttu-id="934d5-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="934d5-126">RELATED LINKS</span></span>

