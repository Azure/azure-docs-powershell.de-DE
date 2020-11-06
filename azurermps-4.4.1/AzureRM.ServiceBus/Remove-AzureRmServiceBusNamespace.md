---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481581"
---
# <span data-ttu-id="789b5-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="789b5-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="789b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="789b5-102">SYNOPSIS</span></span>
<span data-ttu-id="789b5-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="789b5-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="789b5-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="789b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="789b5-105">DESCRIPTION</span></span>
<span data-ttu-id="789b5-106">Das Cmdlet **Remove-AzureRmServiceBusNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="789b5-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="789b5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="789b5-107">EXAMPLES</span></span>

### <span data-ttu-id="789b5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="789b5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="789b5-109">Entfernt den ServiceBus-Namespace `SB-Example1` aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="789b5-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="789b5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="789b5-110">PARAMETERS</span></span>

### <span data-ttu-id="789b5-111">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="789b5-111">-NamespaceName</span></span>
<span data-ttu-id="789b5-112">Der Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="789b5-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="789b5-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="789b5-113">-ResourceGroup</span></span>
<span data-ttu-id="789b5-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="789b5-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="789b5-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="789b5-115">-Confirm</span></span>
<span data-ttu-id="789b5-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="789b5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789b5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789b5-117">-WhatIf</span></span>
<span data-ttu-id="789b5-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="789b5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789b5-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="789b5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789b5-120">CommonParameters</span></span>
<span data-ttu-id="789b5-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789b5-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789b5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789b5-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="789b5-123">INPUTS</span></span>

### <span data-ttu-id="789b5-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="789b5-124">-ResourceGroup</span></span>
 <span data-ttu-id="789b5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="789b5-125">System.String</span></span>

### <span data-ttu-id="789b5-126">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="789b5-126">-NamespaceName</span></span>
 <span data-ttu-id="789b5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="789b5-127">System.String</span></span>

## <span data-ttu-id="789b5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="789b5-128">OUTPUTS</span></span>

### <span data-ttu-id="789b5-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="789b5-129">System.Object</span></span>

## <span data-ttu-id="789b5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="789b5-130">NOTES</span></span>

## <span data-ttu-id="789b5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="789b5-131">RELATED LINKS</span></span>

