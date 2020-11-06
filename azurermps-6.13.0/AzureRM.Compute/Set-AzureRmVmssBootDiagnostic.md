---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: e50b9b1a99c770ca8d9bb88c114a4c80f25283da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477878"
---
# <span data-ttu-id="1a77e-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1a77e-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="1a77e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a77e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a77e-103">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1a77e-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a77e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a77e-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a77e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a77e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a77e-106">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1a77e-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="1a77e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a77e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a77e-108">Beispiel 1: Festlegen der Boot Diagnostics-Profileigenschaft für eine VMSS</span><span class="sxs-lookup"><span data-stu-id="1a77e-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="1a77e-109">Mit diesem Befehl wird die Start Diagnose-Profileigenschaft für die VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a77e-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1a77e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a77e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a77e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a77e-111">-DefaultProfile</span></span>
<span data-ttu-id="1a77e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a77e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a77e-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="1a77e-113">-Enabled</span></span>
<span data-ttu-id="1a77e-114">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a77e-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="1a77e-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1a77e-115">-StorageUri</span></span>
<span data-ttu-id="1a77e-116">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a77e-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="1a77e-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a77e-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1a77e-118">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1a77e-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="1a77e-119">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a77e-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="1a77e-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a77e-120">-Confirm</span></span>
<span data-ttu-id="1a77e-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a77e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a77e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a77e-122">-WhatIf</span></span>
<span data-ttu-id="1a77e-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a77e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a77e-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a77e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a77e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a77e-125">CommonParameters</span></span>
<span data-ttu-id="1a77e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a77e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a77e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a77e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a77e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a77e-128">INPUTS</span></span>

### <span data-ttu-id="1a77e-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a77e-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1a77e-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1a77e-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1a77e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1a77e-131">System.String</span></span>

## <span data-ttu-id="1a77e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a77e-132">OUTPUTS</span></span>

### <span data-ttu-id="1a77e-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a77e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1a77e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a77e-134">NOTES</span></span>

## <span data-ttu-id="1a77e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a77e-135">RELATED LINKS</span></span>
