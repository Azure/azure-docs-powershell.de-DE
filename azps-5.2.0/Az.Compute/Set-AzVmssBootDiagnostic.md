---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294850"
---
# <span data-ttu-id="aad94-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="aad94-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="aad94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad94-102">SYNOPSIS</span></span>
<span data-ttu-id="aad94-103">Legt das Profil für die Startdiagnose für die Skalierungssatz des virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="aad94-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="aad94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aad94-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad94-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aad94-105">DESCRIPTION</span></span>
<span data-ttu-id="aad94-106">Legt das Profil für die Startdiagnose für die Skalierungssatz des virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="aad94-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="aad94-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aad94-107">EXAMPLES</span></span>

### <span data-ttu-id="aad94-108">Beispiel 1: Festlegen der Profileigenschaft für die Startdiagnose für eine VMSS</span><span class="sxs-lookup"><span data-stu-id="aad94-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="aad94-109">Mit diesem Befehl wird die Profileigenschaft für die Startdiagnose für die VMSS namens "ContosoVMSS" bestimmt.</span><span class="sxs-lookup"><span data-stu-id="aad94-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="aad94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad94-110">PARAMETERS</span></span>

### <span data-ttu-id="aad94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad94-111">-DefaultProfile</span></span>
<span data-ttu-id="aad94-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aad94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad94-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="aad94-113">-Enabled</span></span>
<span data-ttu-id="aad94-114">Ob die Startdiagnose für den Skalierungssatz des virtuellen Computers aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aad94-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad94-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="aad94-115">-StorageUri</span></span>
<span data-ttu-id="aad94-116">URI des Speicherkontos, das zum Platzieren der Konsolenausgabe und des Screenshots verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aad94-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad94-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aad94-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="aad94-118">Gibt das "VMSS"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="aad94-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="aad94-119">Sie können das cmdlet New-AzVmssConfig zum Erstellen des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="aad94-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="aad94-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aad94-120">-Confirm</span></span>
<span data-ttu-id="aad94-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aad94-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad94-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aad94-122">-WhatIf</span></span>
<span data-ttu-id="aad94-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aad94-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad94-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aad94-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad94-125">CommonParameters</span></span>
<span data-ttu-id="aad94-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad94-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aad94-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad94-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aad94-128">INPUTS</span></span>

### <span data-ttu-id="aad94-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aad94-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="aad94-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aad94-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aad94-131">System.String</span><span class="sxs-lookup"><span data-stu-id="aad94-131">System.String</span></span>

## <span data-ttu-id="aad94-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aad94-132">OUTPUTS</span></span>

### <span data-ttu-id="aad94-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aad94-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="aad94-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aad94-134">NOTES</span></span>

## <span data-ttu-id="aad94-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aad94-135">RELATED LINKS</span></span>
