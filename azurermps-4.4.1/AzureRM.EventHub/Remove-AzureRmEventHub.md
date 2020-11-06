---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505005"
---
# <span data-ttu-id="8834f-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="8834f-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="8834f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8834f-102">SYNOPSIS</span></span>
<span data-ttu-id="8834f-103">Entfernt den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="8834f-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8834f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8834f-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8834f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8834f-105">DESCRIPTION</span></span>
<span data-ttu-id="8834f-106">Das Remove-AzureRmEventHub-Cmdlet entfernt und löscht den angegebenen Ereignis-Hub aus dem angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="8834f-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="8834f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8834f-107">EXAMPLES</span></span>

### <span data-ttu-id="8834f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8834f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="8834f-109">Entfernt den Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="8834f-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="8834f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8834f-110">PARAMETERS</span></span>

### <span data-ttu-id="8834f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8834f-111">-ResourceGroupName</span></span>
<span data-ttu-id="8834f-112">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8834f-112">Resource group name.</span></span>

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

### <span data-ttu-id="8834f-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8834f-113">-Confirm</span></span>
<span data-ttu-id="8834f-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8834f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8834f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8834f-115">-WhatIf</span></span>
<span data-ttu-id="8834f-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8834f-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8834f-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8834f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8834f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8834f-118">-Name</span></span>
<span data-ttu-id="8834f-119">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="8834f-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8834f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8834f-120">-Namespace</span></span>
<span data-ttu-id="8834f-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8834f-121">Namespace Name.</span></span>

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

## <span data-ttu-id="8834f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8834f-122">INPUTS</span></span>

### <span data-ttu-id="8834f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8834f-123">System.String</span></span>

## <span data-ttu-id="8834f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8834f-124">OUTPUTS</span></span>

### <span data-ttu-id="8834f-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="8834f-125">System.Object</span></span>

## <span data-ttu-id="8834f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8834f-126">NOTES</span></span>

## <span data-ttu-id="8834f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8834f-127">RELATED LINKS</span></span>

