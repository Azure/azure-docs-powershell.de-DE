---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144785"
---
# <span data-ttu-id="13b88-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="13b88-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="13b88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b88-102">SYNOPSIS</span></span>
<span data-ttu-id="13b88-103">Entfernt die Diagnoseerweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="13b88-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="13b88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13b88-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13b88-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13b88-105">DESCRIPTION</span></span>
<span data-ttu-id="13b88-106">Das **Cmdlet "Remove-AzVMDiagnosticsExtension"** entfernt eine Azure-Diagnoseerweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="13b88-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="13b88-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzVM übergeben, um die Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="13b88-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="13b88-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13b88-108">EXAMPLES</span></span>

### <span data-ttu-id="13b88-109">Beispiel 1: Entfernen der Diagnoseerweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="13b88-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="13b88-110">Mit diesem Befehl wird die Diagnoseerweiterung von einem virtuellen Computer namens "ContosoVM22" entfernt.</span><span class="sxs-lookup"><span data-stu-id="13b88-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="13b88-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Update-AzVM an das Update-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b88-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13b88-112">Dieser Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="13b88-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="13b88-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b88-113">PARAMETERS</span></span>

### <span data-ttu-id="13b88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b88-114">-DefaultProfile</span></span>
<span data-ttu-id="13b88-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13b88-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13b88-116">-Name</span><span class="sxs-lookup"><span data-stu-id="13b88-116">-Name</span></span>
<span data-ttu-id="13b88-117">Gibt den Namen der Diagnoseerweiterung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="13b88-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b88-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13b88-118">-NoWait</span></span>
<span data-ttu-id="13b88-119">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="13b88-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="13b88-120">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="13b88-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b88-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b88-121">-ResourceGroupName</span></span>
<span data-ttu-id="13b88-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="13b88-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b88-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="13b88-123">-VMName</span></span>
<span data-ttu-id="13b88-124">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnoseerweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="13b88-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b88-125">CommonParameters</span></span>
<span data-ttu-id="13b88-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b88-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b88-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b88-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13b88-128">INPUTS</span></span>

### <span data-ttu-id="13b88-129">System.String</span><span class="sxs-lookup"><span data-stu-id="13b88-129">System.String</span></span>

## <span data-ttu-id="13b88-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13b88-130">OUTPUTS</span></span>

### <span data-ttu-id="13b88-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="13b88-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="13b88-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13b88-132">NOTES</span></span>

## <span data-ttu-id="13b88-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13b88-133">RELATED LINKS</span></span>

[<span data-ttu-id="13b88-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="13b88-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="13b88-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="13b88-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="13b88-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="13b88-136">Update-AzVM</span></span>](./Update-AzVM.md)


