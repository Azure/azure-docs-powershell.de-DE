---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505021"
---
# <span data-ttu-id="0c37d-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="0c37d-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="0c37d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c37d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c37d-103">Ruft Details zu primären, sekundären connectionStrings und Schlüsseln für die Autorisierungsregel der angegebenen Event Hubs-Namespace Autorisierungsregel ab.</span><span class="sxs-lookup"><span data-stu-id="0c37d-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c37d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c37d-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="0c37d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c37d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c37d-106">Das Get-AzureRmEventHubNamespaceKey-Cmdlet gibt die primären und sekundären connectionStrings-und Schlüssel Details der angegebenen Autorisierungsregel im angegebenen Event Hubs-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="0c37d-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="0c37d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c37d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c37d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c37d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="0c37d-109">Ruft Details zu primären, sekundären connectionStrings und Schlüsseln für die Autorisierungsregel \` MyAuthRuleName \` auf dem Event Hubs-Namespace \` mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0c37d-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0c37d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c37d-110">PARAMETERS</span></span>

### <span data-ttu-id="0c37d-111">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="0c37d-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="0c37d-112">Der Name der Autorisierungsregel für den Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0c37d-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

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

### <span data-ttu-id="0c37d-113">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="0c37d-113">-NamespaceName</span></span>
<span data-ttu-id="0c37d-114">Der Namespacename des Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="0c37d-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="0c37d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c37d-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c37d-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c37d-116">Resource group name.</span></span>

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

## <span data-ttu-id="0c37d-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c37d-117">INPUTS</span></span>

### <span data-ttu-id="0c37d-118">System. String</span><span class="sxs-lookup"><span data-stu-id="0c37d-118">System.String</span></span>

## <span data-ttu-id="0c37d-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c37d-119">OUTPUTS</span></span>

### <span data-ttu-id="0c37d-120">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="0c37d-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="0c37d-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c37d-121">NOTES</span></span>

## <span data-ttu-id="0c37d-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c37d-122">RELATED LINKS</span></span>

