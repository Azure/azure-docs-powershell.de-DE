---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476906"
---
# <span data-ttu-id="e8b46-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8b46-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e8b46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8b46-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b46-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="e8b46-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8b46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8b46-104">SYNTAX</span></span>

### <span data-ttu-id="e8b46-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b46-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8b46-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="e8b46-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8b46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8b46-107">DESCRIPTION</span></span>
<span data-ttu-id="e8b46-108">Das Cmdlet **Update-AzureRmAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="e8b46-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="e8b46-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8b46-109">EXAMPLES</span></span>

### <span data-ttu-id="e8b46-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8b46-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="e8b46-111">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e8b46-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="e8b46-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8b46-112">PARAMETERS</span></span>

### <span data-ttu-id="e8b46-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="e8b46-113">-AvailabilitySet</span></span>
<span data-ttu-id="e8b46-114">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8b46-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b46-115">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="e8b46-115">-Managed</span></span>
<span data-ttu-id="e8b46-116">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="e8b46-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b46-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="e8b46-117">-Sku</span></span>
<span data-ttu-id="e8b46-118">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="e8b46-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b46-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8b46-119">-Confirm</span></span>
<span data-ttu-id="e8b46-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8b46-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b46-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b46-121">-WhatIf</span></span>
<span data-ttu-id="e8b46-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8b46-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8b46-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8b46-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b46-124">CommonParameters</span></span>
<span data-ttu-id="e8b46-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b46-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8b46-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b46-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8b46-127">INPUTS</span></span>

### <span data-ttu-id="e8b46-128">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8b46-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e8b46-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8b46-129">OUTPUTS</span></span>

### <span data-ttu-id="e8b46-130">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8b46-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e8b46-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8b46-131">NOTES</span></span>

## <span data-ttu-id="e8b46-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8b46-132">RELATED LINKS</span></span>

