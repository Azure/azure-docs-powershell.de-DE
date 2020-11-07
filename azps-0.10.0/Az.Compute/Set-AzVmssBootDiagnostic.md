---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 482398d3ba0934f17b1381edc5dac08fb22bd75a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844180"
---
# <span data-ttu-id="894c7-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="894c7-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="894c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="894c7-102">SYNOPSIS</span></span>
<span data-ttu-id="894c7-103">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="894c7-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="894c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="894c7-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="894c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="894c7-105">DESCRIPTION</span></span>
<span data-ttu-id="894c7-106">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="894c7-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="894c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="894c7-107">EXAMPLES</span></span>

### <span data-ttu-id="894c7-108">Beispiel 1: Festlegen der Boot Diagnostics-Profileigenschaft für eine VMSS</span><span class="sxs-lookup"><span data-stu-id="894c7-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="894c7-109">Mit diesem Befehl wird die Start Diagnose-Profileigenschaft für die VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="894c7-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="894c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="894c7-110">PARAMETERS</span></span>

### <span data-ttu-id="894c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894c7-111">-DefaultProfile</span></span>
<span data-ttu-id="894c7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="894c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="894c7-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="894c7-113">-Enabled</span></span>
<span data-ttu-id="894c7-114">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="894c7-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c7-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="894c7-115">-StorageUri</span></span>
<span data-ttu-id="894c7-116">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="894c7-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c7-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="894c7-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="894c7-118">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="894c7-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="894c7-119">Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="894c7-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="894c7-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="894c7-120">-Confirm</span></span>
<span data-ttu-id="894c7-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="894c7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="894c7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894c7-122">-WhatIf</span></span>
<span data-ttu-id="894c7-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="894c7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="894c7-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="894c7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="894c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894c7-125">CommonParameters</span></span>
<span data-ttu-id="894c7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894c7-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894c7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894c7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="894c7-128">INPUTS</span></span>

### <span data-ttu-id="894c7-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="894c7-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="894c7-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="894c7-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="894c7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="894c7-131">OUTPUTS</span></span>

### <span data-ttu-id="894c7-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="894c7-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="894c7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="894c7-133">NOTES</span></span>

## <span data-ttu-id="894c7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="894c7-134">RELATED LINKS</span></span>

