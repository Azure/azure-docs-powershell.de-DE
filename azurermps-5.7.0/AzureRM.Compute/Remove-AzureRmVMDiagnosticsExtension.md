---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483070"
---
# <span data-ttu-id="dc741-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dc741-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="dc741-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc741-102">SYNOPSIS</span></span>
<span data-ttu-id="dc741-103">Entfernt die Diagnose Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dc741-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc741-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc741-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc741-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc741-105">DESCRIPTION</span></span>
<span data-ttu-id="dc741-106">Das Cmdlet **Remove-AzureRmVMDiagnosticsExtension** entfernt eine Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dc741-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="dc741-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzureRmVM-Cmdlet übergeben, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="dc741-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="dc741-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc741-108">EXAMPLES</span></span>

### <span data-ttu-id="dc741-109">Beispiel 1: Entfernen der Diagnose Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="dc741-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="dc741-110">Dieser Befehl entfernt die Diagnose Erweiterung von einem virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="dc741-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="dc741-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Update-AzureRmVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc741-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc741-112">Dieser Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dc741-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="dc741-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc741-113">PARAMETERS</span></span>

### <span data-ttu-id="dc741-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dc741-114">-Name</span></span>
<span data-ttu-id="dc741-115">Gibt den Namen der Diagnostics-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dc741-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc741-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc741-116">-ResourceGroupName</span></span>
<span data-ttu-id="dc741-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="dc741-117">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc741-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="dc741-118">-VMName</span></span>
<span data-ttu-id="dc741-119">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnose Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc741-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc741-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc741-120">CommonParameters</span></span>
<span data-ttu-id="dc741-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc741-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc741-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc741-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc741-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc741-123">INPUTS</span></span>

### <span data-ttu-id="dc741-124">Keine</span><span class="sxs-lookup"><span data-stu-id="dc741-124">None</span></span>
<span data-ttu-id="dc741-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="dc741-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc741-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc741-126">OUTPUTS</span></span>

## <span data-ttu-id="dc741-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc741-127">NOTES</span></span>

## <span data-ttu-id="dc741-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc741-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc741-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dc741-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="dc741-130">Satz-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dc741-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="dc741-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dc741-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


