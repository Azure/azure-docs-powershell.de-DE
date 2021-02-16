---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148780"
---
# <span data-ttu-id="9ee86-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9ee86-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="9ee86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee86-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee86-103">Entfernt eine Diagnoseerweiterung von der VMSS.</span><span class="sxs-lookup"><span data-stu-id="9ee86-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="9ee86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ee86-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ee86-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ee86-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee86-106">Das **Cmdlet "Remove-AzVmssDiagnosticsExtension"** entfernt eine Diagnoseerweiterung aus dem Virtual Machine Scale Set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9ee86-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9ee86-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ee86-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee86-108">Beispiel 1: Entfernen einer Diagnoseerweiterung von der VMSS</span><span class="sxs-lookup"><span data-stu-id="9ee86-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="9ee86-109">Mit diesem Befehl wird die Diagnoseerweiterung von vmSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ee86-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="9ee86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee86-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee86-111">-DefaultProfile</span></span>
<span data-ttu-id="9ee86-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ee86-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ee86-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9ee86-113">-Name</span></span>
<span data-ttu-id="9ee86-114">Gibt den Namen der Erweiterung an, die dieses Cmdlet von der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ee86-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="9ee86-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ee86-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9ee86-116">Gibt die VMSS an, von der die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ee86-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="9ee86-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ee86-117">-Confirm</span></span>
<span data-ttu-id="9ee86-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ee86-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee86-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9ee86-119">-WhatIf</span></span>
<span data-ttu-id="9ee86-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ee86-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee86-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ee86-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee86-122">CommonParameters</span></span>
<span data-ttu-id="9ee86-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee86-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ee86-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee86-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ee86-125">INPUTS</span></span>

### <span data-ttu-id="9ee86-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ee86-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9ee86-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9ee86-127">System.String</span></span>

## <span data-ttu-id="9ee86-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ee86-128">OUTPUTS</span></span>

### <span data-ttu-id="9ee86-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ee86-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9ee86-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ee86-130">NOTES</span></span>

## <span data-ttu-id="9ee86-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ee86-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ee86-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9ee86-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="9ee86-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9ee86-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="9ee86-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9ee86-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


