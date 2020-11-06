---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483158"
---
# <span data-ttu-id="0c47c-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0c47c-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="0c47c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c47c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c47c-103">Entfernt eine Diagnose Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="0c47c-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c47c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c47c-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c47c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c47c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c47c-106">Mit dem Cmdlet **Remove-AzureRmVmssDiagnosticsExtension** wird eine Diagnose Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS) entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c47c-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0c47c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c47c-107">EXAMPLES</span></span>

### <span data-ttu-id="0c47c-108">Beispiel 1: Entfernen einer Diagnose Erweiterung vom VMSS</span><span class="sxs-lookup"><span data-stu-id="0c47c-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="0c47c-109">Dieser Befehl entfernt die Diagnose Erweiterung aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="0c47c-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="0c47c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c47c-110">PARAMETERS</span></span>

### <span data-ttu-id="0c47c-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0c47c-111">-Name</span></span>
<span data-ttu-id="0c47c-112">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c47c-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c47c-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0c47c-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0c47c-114">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c47c-114">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="0c47c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c47c-115">-Confirm</span></span>
<span data-ttu-id="0c47c-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c47c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c47c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c47c-117">-WhatIf</span></span>
<span data-ttu-id="0c47c-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c47c-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0c47c-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c47c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c47c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c47c-120">CommonParameters</span></span>
<span data-ttu-id="0c47c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c47c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c47c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c47c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c47c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c47c-123">INPUTS</span></span>

### <span data-ttu-id="0c47c-124">Keine</span><span class="sxs-lookup"><span data-stu-id="0c47c-124">None</span></span>
<span data-ttu-id="0c47c-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0c47c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c47c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c47c-126">OUTPUTS</span></span>

###  
<span data-ttu-id="0c47c-127">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0c47c-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0c47c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c47c-128">NOTES</span></span>

## <span data-ttu-id="0c47c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c47c-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c47c-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0c47c-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="0c47c-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0c47c-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="0c47c-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0c47c-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


