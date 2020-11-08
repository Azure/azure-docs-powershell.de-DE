---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003864"
---
# <span data-ttu-id="7a2a3-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7a2a3-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="7a2a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2a3-103">Entfernt eine Diagnose Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="7a2a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a2a3-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a2a3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a2a3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a2a3-106">Mit dem Cmdlet **Remove-AzVmssDiagnosticsExtension** wird eine Diagnose Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS) entfernt.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7a2a3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a2a3-107">EXAMPLES</span></span>

### <span data-ttu-id="7a2a3-108">Beispiel 1: Entfernen einer Diagnose Erweiterung vom VMSS</span><span class="sxs-lookup"><span data-stu-id="7a2a3-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="7a2a3-109">Dieser Befehl entfernt die Diagnose Erweiterung aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="7a2a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a2a3-110">PARAMETERS</span></span>

### <span data-ttu-id="7a2a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2a3-111">-DefaultProfile</span></span>
<span data-ttu-id="7a2a3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7a2a3-113">-Name</span></span>
<span data-ttu-id="7a2a3-114">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a3-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7a2a3-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7a2a3-116">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a2a3-117">-Confirm</span></span>
<span data-ttu-id="7a2a3-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2a3-119">-WhatIf</span></span>
<span data-ttu-id="7a2a3-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2a3-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2a3-122">CommonParameters</span></span>
<span data-ttu-id="7a2a3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a2a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2a3-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a2a3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2a3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a2a3-125">INPUTS</span></span>

### <span data-ttu-id="7a2a3-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7a2a3-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7a2a3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7a2a3-127">System.String</span></span>

## <span data-ttu-id="7a2a3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a2a3-128">OUTPUTS</span></span>

### <span data-ttu-id="7a2a3-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7a2a3-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7a2a3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a2a3-130">NOTES</span></span>

## <span data-ttu-id="7a2a3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a2a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="7a2a3-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7a2a3-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="7a2a3-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7a2a3-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="7a2a3-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7a2a3-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


