---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502726"
---
# <span data-ttu-id="0b712-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0b712-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="0b712-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b712-102">SYNOPSIS</span></span>
<span data-ttu-id="0b712-103">Ruft die Details eines Event Hubs-Namespaces ab oder ruft eine Liste aller Event Hubs-Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0b712-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b712-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b712-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="0b712-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b712-105">DESCRIPTION</span></span>
<span data-ttu-id="0b712-106">Das Get-AzureRmEventHubNamespace-Cmdlet ruft entweder die Details eines angegebenen Event Hubs-Namespaces oder eine Liste aller Event Hubs-Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0b712-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="0b712-107">Wenn der Namespacename angegeben wird, werden die Details eines einzelnen Event Hubs-Namespaces zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b712-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="0b712-108">Wenn der Namespacename nicht angegeben wird, wird eine Liste mit Namespaces zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b712-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="0b712-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b712-109">EXAMPLES</span></span>

### <span data-ttu-id="0b712-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b712-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="0b712-111">Ruft die Details des Event Hubs-Namespace \` mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0b712-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0b712-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b712-112">PARAMETERS</span></span>

### <span data-ttu-id="0b712-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b712-113">-ResourceGroupName</span></span>
<span data-ttu-id="0b712-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b712-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b712-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0b712-115">-Name</span></span>
<span data-ttu-id="0b712-116">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="0b712-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="0b712-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b712-117">INPUTS</span></span>

### <span data-ttu-id="0b712-118">System. String</span><span class="sxs-lookup"><span data-stu-id="0b712-118">System.String</span></span>

## <span data-ttu-id="0b712-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b712-119">OUTPUTS</span></span>

### <span data-ttu-id="0b712-120">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0b712-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0b712-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b712-121">NOTES</span></span>

## <span data-ttu-id="0b712-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b712-122">RELATED LINKS</span></span>

