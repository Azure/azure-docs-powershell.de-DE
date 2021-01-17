---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 3f9b425574f8f6d1524d2a4fd9d36c0bb57784f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367463"
---
# <span data-ttu-id="1e64c-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1e64c-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="1e64c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e64c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e64c-103">Ändert die Eigenschaften der Startdiagnose eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1e64c-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="1e64c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e64c-104">SYNTAX</span></span>

### <span data-ttu-id="1e64c-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e64c-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e64c-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e64c-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e64c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e64c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e64c-108">Das **Cmdlet "Set-AzVMBootDiagnostic"** ändert die Eigenschaften der Startdiagnose eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1e64c-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="1e64c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e64c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e64c-110">Beispiel 1: Aktivieren der Startdiagnose</span><span class="sxs-lookup"><span data-stu-id="1e64c-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="1e64c-111">Der erste Befehl ruft den virtuellen Computer "ContosoVM07" mit **"Get-AzVM" ab.**</span><span class="sxs-lookup"><span data-stu-id="1e64c-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="1e64c-112">Der Befehl speichert sie in der $VM Variable.</span><span class="sxs-lookup"><span data-stu-id="1e64c-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="1e64c-113">Der zweite Befehl ermöglicht die Startdiagnose für den virtuellen Computer in $VM.</span><span class="sxs-lookup"><span data-stu-id="1e64c-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="1e64c-114">Diagnosedaten werden im angegebenen Konto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e64c-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="1e64c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e64c-115">PARAMETERS</span></span>

### <span data-ttu-id="1e64c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e64c-116">-DefaultProfile</span></span>
<span data-ttu-id="1e64c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e64c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e64c-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="1e64c-118">-Disable</span></span>
<span data-ttu-id="1e64c-119">Gibt an, dass dieses Cmdlet die Startdiagnose für den virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1e64c-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="1e64c-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="1e64c-120">-Enable</span></span>
<span data-ttu-id="1e64c-121">Gibt an, dass dieses Cmdlet die Startdiagnose für den virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1e64c-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="1e64c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e64c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e64c-123">Gibt den Namen der Ressourcengruppe des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1e64c-123">Specifies the name of the resource group of storage account.</span></span>

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

### <span data-ttu-id="1e64c-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e64c-124">-StorageAccountName</span></span>
<span data-ttu-id="1e64c-125">Gibt den Namen des Speicherkontos an, in dem Startdiagnosedaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1e64c-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="1e64c-126">-VM</span><span class="sxs-lookup"><span data-stu-id="1e64c-126">-VM</span></span>
<span data-ttu-id="1e64c-127">Gibt den virtuellen Computer an, für den dieses Cmdlet die Startdiagnose ändert.</span><span class="sxs-lookup"><span data-stu-id="1e64c-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="1e64c-128">Verwenden Sie zum Abrufen eines Objekts für einen virtuellen Computer das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e64c-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1e64c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e64c-129">CommonParameters</span></span>
<span data-ttu-id="1e64c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e64c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e64c-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e64c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e64c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e64c-132">INPUTS</span></span>

### <span data-ttu-id="1e64c-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1e64c-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1e64c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1e64c-134">System.String</span></span>

## <span data-ttu-id="1e64c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e64c-135">OUTPUTS</span></span>

### <span data-ttu-id="1e64c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1e64c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1e64c-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e64c-137">NOTES</span></span>

## <span data-ttu-id="1e64c-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e64c-138">RELATED LINKS</span></span>

[<span data-ttu-id="1e64c-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e64c-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1e64c-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1e64c-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


