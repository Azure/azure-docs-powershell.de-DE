---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844376"
---
# <span data-ttu-id="31f0a-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="31f0a-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="31f0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="31f0a-103">Entfernt die Diagnose Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="31f0a-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="31f0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31f0a-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f0a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="31f0a-106">Das Cmdlet **Remove-AzVMDiagnosticsExtension** entfernt eine Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="31f0a-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="31f0a-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzVM-Cmdlet übergeben, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="31f0a-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="31f0a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31f0a-108">EXAMPLES</span></span>

### <span data-ttu-id="31f0a-109">Beispiel 1: Entfernen der Diagnose Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="31f0a-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="31f0a-110">Dieser Befehl entfernt die Diagnose Erweiterung von einem virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="31f0a-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="31f0a-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Update-AzVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f0a-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31f0a-112">Dieser Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="31f0a-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="31f0a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="31f0a-113">PARAMETERS</span></span>

### <span data-ttu-id="31f0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f0a-114">-DefaultProfile</span></span>
<span data-ttu-id="31f0a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31f0a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f0a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="31f0a-116">-Name</span></span>
<span data-ttu-id="31f0a-117">Gibt den Namen der Diagnostics-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="31f0a-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="31f0a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f0a-118">-ResourceGroupName</span></span>
<span data-ttu-id="31f0a-119">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="31f0a-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="31f0a-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="31f0a-120">-VMName</span></span>
<span data-ttu-id="31f0a-121">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnose Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="31f0a-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="31f0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f0a-122">CommonParameters</span></span>
<span data-ttu-id="31f0a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f0a-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f0a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f0a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31f0a-125">INPUTS</span></span>

### <span data-ttu-id="31f0a-126">Keine</span><span class="sxs-lookup"><span data-stu-id="31f0a-126">None</span></span>
<span data-ttu-id="31f0a-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="31f0a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31f0a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31f0a-128">OUTPUTS</span></span>

### <span data-ttu-id="31f0a-129">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="31f0a-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="31f0a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="31f0a-130">NOTES</span></span>

## <span data-ttu-id="31f0a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31f0a-131">RELATED LINKS</span></span>

[<span data-ttu-id="31f0a-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="31f0a-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="31f0a-133">Satz-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="31f0a-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="31f0a-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="31f0a-134">Update-AzVM</span></span>](./Update-AzVM.md)


