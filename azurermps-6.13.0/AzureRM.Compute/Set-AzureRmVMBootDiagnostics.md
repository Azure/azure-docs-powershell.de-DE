---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 290c726c53ea4479c4bd1f3cb9b2c607c04f20cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664096"
---
# <span data-ttu-id="fbccc-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fbccc-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="fbccc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbccc-102">SYNOPSIS</span></span>
<span data-ttu-id="fbccc-103">Ändert die Start Diagnoseeigenschaften einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="fbccc-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbccc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbccc-104">SYNTAX</span></span>

### <span data-ttu-id="fbccc-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fbccc-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbccc-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fbccc-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbccc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbccc-107">DESCRIPTION</span></span>
<span data-ttu-id="fbccc-108">Das Cmdlet " **Satz-AzureRmVMBootDiagnostics** " ändert die Eigenschaften der Start Diagnose einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="fbccc-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="fbccc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbccc-109">EXAMPLES</span></span>

### <span data-ttu-id="fbccc-110">Beispiel 1: Aktivieren der Start Diagnose</span><span class="sxs-lookup"><span data-stu-id="fbccc-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="fbccc-111">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoVM07 mithilfe von **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="fbccc-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="fbccc-112">Der Befehl speichert Sie in der $VM-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fbccc-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="fbccc-113">Mit dem zweiten Befehl wird die Start Diagnose für den virtuellen Computer in $VM aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fbccc-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="fbccc-114">Diagnosedaten werden im angegebenen Konto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fbccc-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="fbccc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbccc-115">PARAMETERS</span></span>

### <span data-ttu-id="fbccc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbccc-116">-DefaultProfile</span></span>
<span data-ttu-id="fbccc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbccc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbccc-118">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="fbccc-118">-Disable</span></span>
<span data-ttu-id="fbccc-119">Gibt an, dass dieses Cmdlet die Start Diagnose für den virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fbccc-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbccc-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="fbccc-120">-Enable</span></span>
<span data-ttu-id="fbccc-121">Gibt an, dass dieses Cmdlet die Start Diagnose für den virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fbccc-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbccc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbccc-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbccc-123">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="fbccc-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbccc-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fbccc-124">-StorageAccountName</span></span>
<span data-ttu-id="fbccc-125">Gibt den Namen des speicherkontos an, in dem Start Diagnosedaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fbccc-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbccc-126">-VM</span><span class="sxs-lookup"><span data-stu-id="fbccc-126">-VM</span></span>
<span data-ttu-id="fbccc-127">Gibt den virtuellen Computer an, für den dieses Cmdlet die Start Diagnose ändert.</span><span class="sxs-lookup"><span data-stu-id="fbccc-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="fbccc-128">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fbccc-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbccc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbccc-129">CommonParameters</span></span>
<span data-ttu-id="fbccc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbccc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbccc-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbccc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbccc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbccc-132">INPUTS</span></span>

### <span data-ttu-id="fbccc-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fbccc-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fbccc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fbccc-134">System.String</span></span>

## <span data-ttu-id="fbccc-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbccc-135">OUTPUTS</span></span>

### <span data-ttu-id="fbccc-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fbccc-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fbccc-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbccc-137">NOTES</span></span>

## <span data-ttu-id="fbccc-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbccc-138">RELATED LINKS</span></span>

[<span data-ttu-id="fbccc-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fbccc-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="fbccc-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="fbccc-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


