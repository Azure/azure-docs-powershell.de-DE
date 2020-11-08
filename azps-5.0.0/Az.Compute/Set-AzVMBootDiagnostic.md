---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 3f9b425574f8f6d1524d2a4fd9d36c0bb57784f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177701"
---
# <span data-ttu-id="b186f-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b186f-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="b186f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b186f-102">SYNOPSIS</span></span>
<span data-ttu-id="b186f-103">Ändert die Start Diagnoseeigenschaften einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="b186f-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="b186f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b186f-104">SYNTAX</span></span>

### <span data-ttu-id="b186f-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b186f-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b186f-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b186f-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b186f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b186f-107">DESCRIPTION</span></span>
<span data-ttu-id="b186f-108">Das Cmdlet " **Satz-AzVMBootDiagnostic** " ändert die Eigenschaften der Start Diagnose einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="b186f-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="b186f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b186f-109">EXAMPLES</span></span>

### <span data-ttu-id="b186f-110">Beispiel 1: Aktivieren der Start Diagnose</span><span class="sxs-lookup"><span data-stu-id="b186f-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="b186f-111">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoVM07 mithilfe von **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="b186f-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="b186f-112">Der Befehl speichert Sie in der $VM-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b186f-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="b186f-113">Mit dem zweiten Befehl wird die Start Diagnose für den virtuellen Computer in $VM aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b186f-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="b186f-114">Diagnosedaten werden im angegebenen Konto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b186f-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="b186f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b186f-115">PARAMETERS</span></span>

### <span data-ttu-id="b186f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b186f-116">-DefaultProfile</span></span>
<span data-ttu-id="b186f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b186f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b186f-118">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="b186f-118">-Disable</span></span>
<span data-ttu-id="b186f-119">Gibt an, dass dieses Cmdlet die Start Diagnose für den virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b186f-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="b186f-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="b186f-120">-Enable</span></span>
<span data-ttu-id="b186f-121">Gibt an, dass dieses Cmdlet die Start Diagnose für den virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b186f-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="b186f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b186f-122">-ResourceGroupName</span></span>
<span data-ttu-id="b186f-123">Gibt den Namen der Ressourcengruppe des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="b186f-123">Specifies the name of the resource group of storage account.</span></span>

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

### <span data-ttu-id="b186f-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b186f-124">-StorageAccountName</span></span>
<span data-ttu-id="b186f-125">Gibt den Namen des speicherkontos an, in dem Start Diagnosedaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b186f-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="b186f-126">-VM</span><span class="sxs-lookup"><span data-stu-id="b186f-126">-VM</span></span>
<span data-ttu-id="b186f-127">Gibt den virtuellen Computer an, für den dieses Cmdlet die Start Diagnose ändert.</span><span class="sxs-lookup"><span data-stu-id="b186f-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="b186f-128">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b186f-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="b186f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b186f-129">CommonParameters</span></span>
<span data-ttu-id="b186f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b186f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b186f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b186f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b186f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b186f-132">INPUTS</span></span>

### <span data-ttu-id="b186f-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b186f-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b186f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b186f-134">System.String</span></span>

## <span data-ttu-id="b186f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b186f-135">OUTPUTS</span></span>

### <span data-ttu-id="b186f-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b186f-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b186f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b186f-137">NOTES</span></span>

## <span data-ttu-id="b186f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b186f-138">RELATED LINKS</span></span>

[<span data-ttu-id="b186f-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b186f-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b186f-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="b186f-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


