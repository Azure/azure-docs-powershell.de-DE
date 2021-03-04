---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: a163854838dcb8e41b7a8b65d1be9e1aca088d55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938267"
---
# <span data-ttu-id="888d1-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="888d1-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="888d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="888d1-102">SYNOPSIS</span></span>
<span data-ttu-id="888d1-103">Ändert die Eigenschaften der Startdiagnose eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="888d1-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="888d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="888d1-104">SYNTAX</span></span>

### <span data-ttu-id="888d1-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="888d1-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="888d1-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="888d1-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="888d1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="888d1-107">DESCRIPTION</span></span>
<span data-ttu-id="888d1-108">Das **Cmdlet Set-AzVMBootDiagnostic** ändert die Eigenschaften der Startdiagnose eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="888d1-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="888d1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="888d1-109">EXAMPLES</span></span>

### <span data-ttu-id="888d1-110">Beispiel 1: Aktivieren der Startdiagnose</span><span class="sxs-lookup"><span data-stu-id="888d1-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="888d1-111">Der erste Befehl ruft den virtuellen Computer namens ContosoVM07 mithilfe von **Get-AzVM ab.**</span><span class="sxs-lookup"><span data-stu-id="888d1-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="888d1-112">Der Befehl speichert ihn in der $VM-Variable.</span><span class="sxs-lookup"><span data-stu-id="888d1-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="888d1-113">Der zweite Befehl ermöglicht die Startdiagnose für den virtuellen Computer in $VM.</span><span class="sxs-lookup"><span data-stu-id="888d1-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="888d1-114">Diagnosedaten werden im angegebenen Konto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="888d1-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="888d1-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="888d1-115">PARAMETERS</span></span>

### <span data-ttu-id="888d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888d1-116">-DefaultProfile</span></span>
<span data-ttu-id="888d1-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="888d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="888d1-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="888d1-118">-Disable</span></span>
<span data-ttu-id="888d1-119">Gibt an, dass dieses Cmdlet die Startdiagnose für den virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="888d1-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="888d1-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="888d1-120">-Enable</span></span>
<span data-ttu-id="888d1-121">Gibt an, dass dieses Cmdlet die Startdiagnose für den virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="888d1-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="888d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="888d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="888d1-123">Gibt den Namen der Ressourcengruppe des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="888d1-123">Specifies the name of the resource group of storage account.</span></span>

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

### <span data-ttu-id="888d1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="888d1-124">-StorageAccountName</span></span>
<span data-ttu-id="888d1-125">Gibt den Namen des Speicherkontos an, in dem Startdiagnosedaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="888d1-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="888d1-126">-VM</span><span class="sxs-lookup"><span data-stu-id="888d1-126">-VM</span></span>
<span data-ttu-id="888d1-127">Gibt den virtuellen Computer an, für den dieses Cmdlet die Startdiagnose ändert.</span><span class="sxs-lookup"><span data-stu-id="888d1-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="888d1-128">Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="888d1-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="888d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888d1-129">CommonParameters</span></span>
<span data-ttu-id="888d1-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="888d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888d1-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="888d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888d1-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="888d1-132">INPUTS</span></span>

### <span data-ttu-id="888d1-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="888d1-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="888d1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="888d1-134">System.String</span></span>

## <span data-ttu-id="888d1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="888d1-135">OUTPUTS</span></span>

### <span data-ttu-id="888d1-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="888d1-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="888d1-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="888d1-137">NOTES</span></span>

## <span data-ttu-id="888d1-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="888d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="888d1-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="888d1-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="888d1-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="888d1-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


