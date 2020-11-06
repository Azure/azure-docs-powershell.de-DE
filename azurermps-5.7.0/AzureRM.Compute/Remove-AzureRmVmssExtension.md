---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483062"
---
# <span data-ttu-id="81988-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="81988-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="81988-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81988-102">SYNOPSIS</span></span>
<span data-ttu-id="81988-103">Entfernt eine Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="81988-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81988-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81988-104">SYNTAX</span></span>

### <span data-ttu-id="81988-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="81988-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81988-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81988-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81988-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81988-107">DESCRIPTION</span></span>
<span data-ttu-id="81988-108">Das Cmdlet **Remove-AzureRmVmssExtension** entfernt eine Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS).</span><span class="sxs-lookup"><span data-stu-id="81988-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="81988-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81988-109">EXAMPLES</span></span>

## <span data-ttu-id="81988-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="81988-110">PARAMETERS</span></span>

### <span data-ttu-id="81988-111">-ID</span><span class="sxs-lookup"><span data-stu-id="81988-111">-Id</span></span>
<span data-ttu-id="81988-112">Gibt die ID der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="81988-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81988-113">-Name</span><span class="sxs-lookup"><span data-stu-id="81988-113">-Name</span></span>
<span data-ttu-id="81988-114">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="81988-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81988-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="81988-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="81988-116">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="81988-116">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81988-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81988-117">-Confirm</span></span>
<span data-ttu-id="81988-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81988-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81988-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81988-119">-WhatIf</span></span>
<span data-ttu-id="81988-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81988-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81988-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81988-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81988-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81988-122">CommonParameters</span></span>
<span data-ttu-id="81988-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81988-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81988-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81988-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81988-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81988-125">INPUTS</span></span>

### <span data-ttu-id="81988-126">Keine</span><span class="sxs-lookup"><span data-stu-id="81988-126">None</span></span>
<span data-ttu-id="81988-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="81988-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81988-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81988-128">OUTPUTS</span></span>

### <span data-ttu-id="81988-129">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="81988-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="81988-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="81988-130">NOTES</span></span>

## <span data-ttu-id="81988-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81988-131">RELATED LINKS</span></span>

[<span data-ttu-id="81988-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="81988-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
