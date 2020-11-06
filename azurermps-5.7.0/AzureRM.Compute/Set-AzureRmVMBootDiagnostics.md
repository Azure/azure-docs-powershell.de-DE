---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481313"
---
# <span data-ttu-id="bce46-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bce46-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="bce46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bce46-102">SYNOPSIS</span></span>
<span data-ttu-id="bce46-103">Ändert die Start Diagnoseeigenschaften einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="bce46-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bce46-104">SYNTAX</span></span>

### <span data-ttu-id="bce46-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bce46-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="bce46-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bce46-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="bce46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bce46-107">DESCRIPTION</span></span>
<span data-ttu-id="bce46-108">Das Cmdlet " **Satz-AzureRmVMBootDiagnostics** " ändert die Eigenschaften der Start Diagnose einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="bce46-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="bce46-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bce46-109">EXAMPLES</span></span>

### <span data-ttu-id="bce46-110">Beispiel 1: Aktivieren der Start Diagnose</span><span class="sxs-lookup"><span data-stu-id="bce46-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="bce46-111">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoVM07 mithilfe von **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="bce46-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="bce46-112">Der Befehl speichert Sie in der $VM-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bce46-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="bce46-113">Mit dem zweiten Befehl wird die Start Diagnose für den virtuellen Computer in $VM aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bce46-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="bce46-114">Diagnosedaten werden im angegebenen Konto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bce46-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="bce46-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bce46-115">PARAMETERS</span></span>

### <span data-ttu-id="bce46-116">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="bce46-116">-Disable</span></span>
<span data-ttu-id="bce46-117">Gibt an, dass dieses Cmdlet die Start Diagnose für den virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bce46-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce46-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="bce46-118">-Enable</span></span>
<span data-ttu-id="bce46-119">Gibt an, dass dieses Cmdlet die Start Diagnose für den virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bce46-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce46-120">-ResourceGroupName</span></span>
<span data-ttu-id="bce46-121">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="bce46-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce46-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bce46-122">-StorageAccountName</span></span>
<span data-ttu-id="bce46-123">Gibt den Namen des speicherkontos an, in dem Start Diagnosedaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bce46-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce46-124">-VM</span><span class="sxs-lookup"><span data-stu-id="bce46-124">-VM</span></span>
<span data-ttu-id="bce46-125">Gibt den virtuellen Computer an, für den dieses Cmdlet die Start Diagnose ändert.</span><span class="sxs-lookup"><span data-stu-id="bce46-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="bce46-126">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bce46-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bce46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce46-127">CommonParameters</span></span>
<span data-ttu-id="bce46-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce46-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce46-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce46-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bce46-130">INPUTS</span></span>

### <span data-ttu-id="bce46-131">Keine</span><span class="sxs-lookup"><span data-stu-id="bce46-131">None</span></span>
<span data-ttu-id="bce46-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bce46-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bce46-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bce46-133">OUTPUTS</span></span>

## <span data-ttu-id="bce46-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="bce46-134">NOTES</span></span>

## <span data-ttu-id="bce46-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bce46-135">RELATED LINKS</span></span>

[<span data-ttu-id="bce46-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bce46-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="bce46-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="bce46-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


