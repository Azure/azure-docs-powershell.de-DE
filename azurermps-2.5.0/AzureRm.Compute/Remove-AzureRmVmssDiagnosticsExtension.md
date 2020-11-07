---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 74bb0bee84615618f464cfbfd86dcb2b7dde387b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850048"
---
# <span data-ttu-id="c8c90-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8c90-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="c8c90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8c90-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c90-103">Entfernt eine Diagnose Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8c90-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8c90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8c90-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8c90-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c90-106">Mit dem Cmdlet **Remove-AzureRmVmssDiagnosticsExtension** wird eine Diagnose Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS) entfernt.</span><span class="sxs-lookup"><span data-stu-id="c8c90-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c8c90-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8c90-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c90-108">Beispiel 1: Entfernen einer Diagnose Erweiterung vom VMSS</span><span class="sxs-lookup"><span data-stu-id="c8c90-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="c8c90-109">Dieser Befehl entfernt die Diagnose Erweiterung aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8c90-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="c8c90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8c90-110">PARAMETERS</span></span>

### <span data-ttu-id="c8c90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c90-111">-DefaultProfile</span></span>
<span data-ttu-id="c8c90-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8c90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8c90-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c8c90-113">-Name</span></span>
<span data-ttu-id="c8c90-114">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="c8c90-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="c8c90-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8c90-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c8c90-116">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8c90-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="c8c90-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8c90-117">-Confirm</span></span>
<span data-ttu-id="c8c90-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8c90-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c90-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c90-119">-WhatIf</span></span>
<span data-ttu-id="c8c90-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8c90-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c8c90-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8c90-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c90-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c90-122">CommonParameters</span></span>
<span data-ttu-id="c8c90-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c90-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c90-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c90-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c90-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8c90-125">INPUTS</span></span>

### <span data-ttu-id="c8c90-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8c90-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="c8c90-127">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8c90-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="c8c90-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8c90-128">OUTPUTS</span></span>

###  
<span data-ttu-id="c8c90-129">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c8c90-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c8c90-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8c90-130">NOTES</span></span>

## <span data-ttu-id="c8c90-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8c90-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8c90-132">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8c90-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="c8c90-133">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8c90-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="c8c90-134">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c8c90-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


