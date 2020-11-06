---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500046"
---
# <span data-ttu-id="35c43-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="35c43-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="35c43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35c43-102">SYNOPSIS</span></span>
<span data-ttu-id="35c43-103">Entfernt den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="35c43-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35c43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c43-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="35c43-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35c43-105">DESCRIPTION</span></span>
<span data-ttu-id="35c43-106">Das Remove-AzureRmEventHubNamespace-Cmdlet entfernt den angegebenen Event Hubs-Namespace und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="35c43-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="35c43-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c43-107">EXAMPLES</span></span>

### <span data-ttu-id="35c43-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35c43-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="35c43-109">Entfernt den Event Hubs \` -Namespace mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="35c43-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="35c43-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c43-110">PARAMETERS</span></span>

### <span data-ttu-id="35c43-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c43-111">-ResourceGroupName</span></span>
<span data-ttu-id="35c43-112">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35c43-112">Resource group name.</span></span>

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

### <span data-ttu-id="35c43-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35c43-113">-Confirm</span></span>
<span data-ttu-id="35c43-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35c43-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c43-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c43-115">-WhatIf</span></span>
<span data-ttu-id="35c43-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35c43-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35c43-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35c43-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c43-118">-Name</span><span class="sxs-lookup"><span data-stu-id="35c43-118">-Name</span></span>
<span data-ttu-id="35c43-119">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="35c43-119">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="35c43-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35c43-120">INPUTS</span></span>

### <span data-ttu-id="35c43-121">System. String</span><span class="sxs-lookup"><span data-stu-id="35c43-121">System.String</span></span>

## <span data-ttu-id="35c43-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35c43-122">OUTPUTS</span></span>

### <span data-ttu-id="35c43-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="35c43-123">System.Object</span></span>

## <span data-ttu-id="35c43-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="35c43-124">NOTES</span></span>

## <span data-ttu-id="35c43-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35c43-125">RELATED LINKS</span></span>

