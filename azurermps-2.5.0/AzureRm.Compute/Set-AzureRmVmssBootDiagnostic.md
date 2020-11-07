---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848323"
---
# <span data-ttu-id="a89b6-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a89b6-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="a89b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a89b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a89b6-103">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a89b6-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a89b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a89b6-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a89b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a89b6-105">DESCRIPTION</span></span>
<span data-ttu-id="a89b6-106">Legt das Start Diagnose Profil für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a89b6-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="a89b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a89b6-107">EXAMPLES</span></span>

### <span data-ttu-id="a89b6-108">Beispiel 1: Festlegen der Boot Diagnostics-Profileigenschaft für eine VMSS</span><span class="sxs-lookup"><span data-stu-id="a89b6-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="a89b6-109">Mit diesem Befehl wird die Start Diagnose-Profileigenschaft für die VMSS mit dem Namen ContosoVMSS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a89b6-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a89b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a89b6-110">PARAMETERS</span></span>

### <span data-ttu-id="a89b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89b6-111">-DefaultProfile</span></span>
<span data-ttu-id="a89b6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a89b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a89b6-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="a89b6-113">-Enabled</span></span>
<span data-ttu-id="a89b6-114">Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a89b6-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="a89b6-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a89b6-115">-StorageUri</span></span>
<span data-ttu-id="a89b6-116">Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a89b6-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="a89b6-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a89b6-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a89b6-118">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a89b6-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="a89b6-119">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a89b6-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a89b6-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a89b6-120">-Confirm</span></span>
<span data-ttu-id="a89b6-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a89b6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a89b6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89b6-122">-WhatIf</span></span>
<span data-ttu-id="a89b6-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a89b6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a89b6-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a89b6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a89b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89b6-125">CommonParameters</span></span>
<span data-ttu-id="a89b6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a89b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89b6-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89b6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89b6-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a89b6-128">INPUTS</span></span>

### <span data-ttu-id="a89b6-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a89b6-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="a89b6-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="a89b6-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="a89b6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a89b6-131">OUTPUTS</span></span>

### <span data-ttu-id="a89b6-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a89b6-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="a89b6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a89b6-133">NOTES</span></span>

## <span data-ttu-id="a89b6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a89b6-134">RELATED LINKS</span></span>

