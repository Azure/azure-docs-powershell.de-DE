---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173288"
---
# <span data-ttu-id="d83f9-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d83f9-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="d83f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d83f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d83f9-103">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d83f9-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d83f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d83f9-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d83f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d83f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d83f9-106">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d83f9-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d83f9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d83f9-107">EXAMPLES</span></span>

### <span data-ttu-id="d83f9-108">Beispiel 1: Festlegen der Boot Diagnostics-Profileigenschaft für eine VMSS</span><span class="sxs-lookup"><span data-stu-id="d83f9-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="d83f9-109">Mit diesem Befehl wird die Start Diagnose-Profileigenschaft für die VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d83f9-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d83f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d83f9-110">PARAMETERS</span></span>

### <span data-ttu-id="d83f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83f9-111">-DefaultProfile</span></span>
<span data-ttu-id="d83f9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d83f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d83f9-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d83f9-113">-Enabled</span></span>
<span data-ttu-id="d83f9-114">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d83f9-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d83f9-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d83f9-115">-StorageUri</span></span>
<span data-ttu-id="d83f9-116">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d83f9-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="d83f9-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d83f9-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d83f9-118">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d83f9-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="d83f9-119">Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d83f9-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d83f9-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d83f9-120">-Confirm</span></span>
<span data-ttu-id="d83f9-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d83f9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83f9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83f9-122">-WhatIf</span></span>
<span data-ttu-id="d83f9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d83f9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d83f9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d83f9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d83f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83f9-125">CommonParameters</span></span>
<span data-ttu-id="d83f9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83f9-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d83f9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83f9-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d83f9-128">INPUTS</span></span>

### <span data-ttu-id="d83f9-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d83f9-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d83f9-130">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d83f9-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d83f9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d83f9-131">System.String</span></span>

## <span data-ttu-id="d83f9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d83f9-132">OUTPUTS</span></span>

### <span data-ttu-id="d83f9-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d83f9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d83f9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d83f9-134">NOTES</span></span>

## <span data-ttu-id="d83f9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d83f9-135">RELATED LINKS</span></span>
