---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008320"
---
# <span data-ttu-id="973a1-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="973a1-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="973a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="973a1-102">SYNOPSIS</span></span>
<span data-ttu-id="973a1-103">Entfernt die Diagnose Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="973a1-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="973a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="973a1-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="973a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="973a1-105">DESCRIPTION</span></span>
<span data-ttu-id="973a1-106">Das Cmdlet **Remove-AzVMDiagnosticsExtension** entfernt eine Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="973a1-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="973a1-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzVM-Cmdlet übergeben, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="973a1-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="973a1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="973a1-108">EXAMPLES</span></span>

### <span data-ttu-id="973a1-109">Beispiel 1: Entfernen der Diagnose Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="973a1-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="973a1-110">Dieser Befehl entfernt die Diagnose Erweiterung von einem virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="973a1-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="973a1-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Update-AzVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="973a1-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="973a1-112">Dieser Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="973a1-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="973a1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="973a1-113">PARAMETERS</span></span>

### <span data-ttu-id="973a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973a1-114">-DefaultProfile</span></span>
<span data-ttu-id="973a1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="973a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="973a1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="973a1-116">-Name</span></span>
<span data-ttu-id="973a1-117">Gibt den Namen der Diagnostics-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="973a1-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="973a1-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="973a1-118">-NoWait</span></span>
<span data-ttu-id="973a1-119">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="973a1-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="973a1-120">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="973a1-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="973a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="973a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="973a1-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="973a1-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="973a1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="973a1-123">-VMName</span></span>
<span data-ttu-id="973a1-124">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnose Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="973a1-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="973a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973a1-125">CommonParameters</span></span>
<span data-ttu-id="973a1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="973a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973a1-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="973a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973a1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="973a1-128">INPUTS</span></span>

### <span data-ttu-id="973a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="973a1-129">System.String</span></span>

## <span data-ttu-id="973a1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="973a1-130">OUTPUTS</span></span>

### <span data-ttu-id="973a1-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="973a1-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="973a1-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="973a1-132">NOTES</span></span>

## <span data-ttu-id="973a1-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="973a1-133">RELATED LINKS</span></span>

[<span data-ttu-id="973a1-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="973a1-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="973a1-135">Satz-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="973a1-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="973a1-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="973a1-136">Update-AzVM</span></span>](./Update-AzVM.md)


