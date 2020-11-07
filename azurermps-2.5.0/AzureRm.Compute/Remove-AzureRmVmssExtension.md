---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848328"
---
# <span data-ttu-id="d39f2-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d39f2-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="d39f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d39f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d39f2-103">Entfernt eine Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="d39f2-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d39f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d39f2-104">SYNTAX</span></span>

### <span data-ttu-id="d39f2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d39f2-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d39f2-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d39f2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d39f2-107">DESCRIPTION</span></span>
<span data-ttu-id="d39f2-108">Das Cmdlet **Remove-AzureRmVmssExtension** entfernt eine Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d39f2-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d39f2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d39f2-109">EXAMPLES</span></span>

## <span data-ttu-id="d39f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d39f2-110">PARAMETERS</span></span>

### <span data-ttu-id="d39f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39f2-111">-DefaultProfile</span></span>
<span data-ttu-id="d39f2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d39f2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f2-113">-ID</span><span class="sxs-lookup"><span data-stu-id="d39f2-113">-Id</span></span>
<span data-ttu-id="d39f2-114">Gibt die ID der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="d39f2-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="d39f2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d39f2-115">-Name</span></span>
<span data-ttu-id="d39f2-116">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="d39f2-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="d39f2-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d39f2-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d39f2-118">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d39f2-118">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39f2-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d39f2-119">-Confirm</span></span>
<span data-ttu-id="d39f2-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d39f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39f2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39f2-121">-WhatIf</span></span>
<span data-ttu-id="d39f2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d39f2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d39f2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d39f2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39f2-124">CommonParameters</span></span>
<span data-ttu-id="d39f2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39f2-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39f2-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d39f2-127">INPUTS</span></span>

### <span data-ttu-id="d39f2-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d39f2-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d39f2-129">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d39f2-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d39f2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d39f2-130">OUTPUTS</span></span>

### <span data-ttu-id="d39f2-131">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d39f2-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d39f2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d39f2-132">NOTES</span></span>

## <span data-ttu-id="d39f2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d39f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="d39f2-134">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d39f2-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
