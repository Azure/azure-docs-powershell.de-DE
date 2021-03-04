---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5b5a27be50da8a9c05b0cf766d48efe5844a0452
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947216"
---
# <span data-ttu-id="273fc-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="273fc-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="273fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="273fc-102">SYNOPSIS</span></span>
<span data-ttu-id="273fc-103">Entfernt die Diagnoseerweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="273fc-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="273fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="273fc-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="273fc-105">DESCRIPTION</span></span>
<span data-ttu-id="273fc-106">Das **Cmdlet Remove-AzVMDiagnosticsExtension** entfernt eine Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="273fc-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="273fc-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzVM übergeben, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="273fc-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="273fc-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="273fc-108">EXAMPLES</span></span>

### <span data-ttu-id="273fc-109">Beispiel 1: Entfernen der Diagnoseerweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="273fc-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="273fc-110">Mit diesem Befehl wird die Diagnoseerweiterung von einem virtuellen Computer namens ContosoVM22 entfernt.</span><span class="sxs-lookup"><span data-stu-id="273fc-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="273fc-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Update-AzVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="273fc-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="273fc-112">Mit diesem Befehl wird der virtuelle Computer aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="273fc-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="273fc-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="273fc-113">PARAMETERS</span></span>

### <span data-ttu-id="273fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273fc-114">-DefaultProfile</span></span>
<span data-ttu-id="273fc-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="273fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="273fc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="273fc-116">-Name</span></span>
<span data-ttu-id="273fc-117">Gibt den Namen der Diagnoseerweiterung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="273fc-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="273fc-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="273fc-118">-NoWait</span></span>
<span data-ttu-id="273fc-119">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="273fc-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="273fc-120">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="273fc-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="273fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="273fc-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="273fc-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="273fc-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="273fc-123">-VMName</span></span>
<span data-ttu-id="273fc-124">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnoseerweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="273fc-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="273fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273fc-125">CommonParameters</span></span>
<span data-ttu-id="273fc-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="273fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273fc-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="273fc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273fc-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="273fc-128">INPUTS</span></span>

### <span data-ttu-id="273fc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="273fc-129">System.String</span></span>

## <span data-ttu-id="273fc-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="273fc-130">OUTPUTS</span></span>

### <span data-ttu-id="273fc-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="273fc-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="273fc-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="273fc-132">NOTES</span></span>

## <span data-ttu-id="273fc-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="273fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="273fc-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="273fc-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="273fc-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="273fc-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="273fc-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="273fc-136">Update-AzVM</span></span>](./Update-AzVM.md)


