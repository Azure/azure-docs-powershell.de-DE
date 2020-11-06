---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505041"
---
# <span data-ttu-id="8e2c9-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="8e2c9-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="8e2c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2c9-103">Ruft die Details eines einzelnen Ereignis Hubs ab oder ruft eine Liste der Ereignis Hubs ab.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e2c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e2c9-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="8e2c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e2c9-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2c9-106">Das Get-AzureRmEventHub-Cmdlet gibt entweder die Details eines Event-Hubs oder eine Liste aller Event-Hubs im aktuellen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="8e2c9-107">Wenn der Name des Ereignis Hubs bereitgestellt wird, werden die Details eines einzelnen Ereignis Hubs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="8e2c9-108">Wenn kein Ereignis-Hub-Name angegeben wird, wird eine Liste aller Ereignis Hubs im angegebenen Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="8e2c9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e2c9-109">EXAMPLES</span></span>

### <span data-ttu-id="8e2c9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e2c9-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8e2c9-111">Gibt die Details des Ereignis-Hub \` -MyEventHubName zurück \` .</span><span class="sxs-lookup"><span data-stu-id="8e2c9-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="8e2c9-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e2c9-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="8e2c9-113">Gibt eine Liste von Ereignis Hubs im Namespace \` mynamespacename zurück \` .</span><span class="sxs-lookup"><span data-stu-id="8e2c9-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8e2c9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e2c9-114">PARAMETERS</span></span>

### <span data-ttu-id="8e2c9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2c9-115">-ResourceGroupName</span></span>
<span data-ttu-id="8e2c9-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-116">Resource group name.</span></span>

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

### <span data-ttu-id="8e2c9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8e2c9-117">-Name</span></span>
<span data-ttu-id="8e2c9-118">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2c9-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8e2c9-119">-Namespace</span></span>
<span data-ttu-id="8e2c9-120">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="8e2c9-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e2c9-121">INPUTS</span></span>

### <span data-ttu-id="8e2c9-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8e2c9-122">System.String</span></span>

## <span data-ttu-id="8e2c9-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e2c9-123">OUTPUTS</span></span>

### <span data-ttu-id="8e2c9-124">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8e2c9-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8e2c9-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e2c9-125">NOTES</span></span>

## <span data-ttu-id="8e2c9-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e2c9-126">RELATED LINKS</span></span>

