---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996806"
---
# <span data-ttu-id="9bf12-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9bf12-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="9bf12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bf12-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf12-103">Entfernt die Diagnose Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9bf12-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="9bf12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bf12-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf12-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bf12-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf12-106">Das Cmdlet **Remove-AzVMDiagnosticsExtension** entfernt eine Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9bf12-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="9bf12-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzVM-Cmdlet übergeben, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9bf12-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="9bf12-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bf12-108">EXAMPLES</span></span>

### <span data-ttu-id="9bf12-109">Beispiel 1: Entfernen der Diagnose Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9bf12-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="9bf12-110">Dieser Befehl entfernt die Diagnose Erweiterung von einem virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="9bf12-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="9bf12-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Update-AzVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf12-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9bf12-112">Dieser Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9bf12-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="9bf12-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bf12-113">PARAMETERS</span></span>

### <span data-ttu-id="9bf12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf12-114">-DefaultProfile</span></span>
<span data-ttu-id="9bf12-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9bf12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf12-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9bf12-116">-Name</span></span>
<span data-ttu-id="9bf12-117">Gibt den Namen der Diagnostics-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9bf12-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bf12-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9bf12-118">-NoWait</span></span>
<span data-ttu-id="9bf12-119">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="9bf12-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9bf12-120">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9bf12-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9bf12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf12-121">-ResourceGroupName</span></span>
<span data-ttu-id="9bf12-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9bf12-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9bf12-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="9bf12-123">-VMName</span></span>
<span data-ttu-id="9bf12-124">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnose Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="9bf12-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="9bf12-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf12-125">CommonParameters</span></span>
<span data-ttu-id="9bf12-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf12-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf12-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf12-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf12-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bf12-128">INPUTS</span></span>

### <span data-ttu-id="9bf12-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf12-129">System.String</span></span>

## <span data-ttu-id="9bf12-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bf12-130">OUTPUTS</span></span>

### <span data-ttu-id="9bf12-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9bf12-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9bf12-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bf12-132">NOTES</span></span>

## <span data-ttu-id="9bf12-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bf12-133">RELATED LINKS</span></span>

[<span data-ttu-id="9bf12-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9bf12-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="9bf12-135">Satz-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9bf12-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="9bf12-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9bf12-136">Update-AzVM</span></span>](./Update-AzVM.md)


