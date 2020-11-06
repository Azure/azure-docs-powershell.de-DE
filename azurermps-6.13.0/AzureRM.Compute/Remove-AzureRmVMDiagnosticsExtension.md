---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 4a14c5138a0dac983067e6deb4b1e05b88d85259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502205"
---
# <span data-ttu-id="cbea1-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cbea1-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="cbea1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cbea1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbea1-103">Entfernt die Diagnose Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cbea1-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbea1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbea1-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbea1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbea1-105">DESCRIPTION</span></span>
<span data-ttu-id="cbea1-106">Das Cmdlet **Remove-AzureRmVMDiagnosticsExtension** entfernt eine Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cbea1-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="cbea1-107">Sie müssen die Ausgabe dieses Cmdlets an das Update-AzureRmVM-Cmdlet übergeben, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="cbea1-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="cbea1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbea1-108">EXAMPLES</span></span>

### <span data-ttu-id="cbea1-109">Beispiel 1: Entfernen der Diagnose Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="cbea1-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="cbea1-110">Dieser Befehl entfernt die Diagnose Erweiterung von einem virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="cbea1-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="cbea1-111">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Update-AzureRmVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbea1-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cbea1-112">Dieser Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cbea1-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="cbea1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbea1-113">PARAMETERS</span></span>

### <span data-ttu-id="cbea1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbea1-114">-DefaultProfile</span></span>
<span data-ttu-id="cbea1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cbea1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbea1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cbea1-116">-Name</span></span>
<span data-ttu-id="cbea1-117">Gibt den Namen der Diagnostics-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cbea1-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbea1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbea1-118">-ResourceGroupName</span></span>
<span data-ttu-id="cbea1-119">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="cbea1-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cbea1-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="cbea1-120">-VMName</span></span>
<span data-ttu-id="cbea1-121">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet eine Diagnose Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="cbea1-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="cbea1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbea1-122">CommonParameters</span></span>
<span data-ttu-id="cbea1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbea1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbea1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbea1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbea1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cbea1-125">INPUTS</span></span>

### <span data-ttu-id="cbea1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cbea1-126">System.String</span></span>

## <span data-ttu-id="cbea1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cbea1-127">OUTPUTS</span></span>

### <span data-ttu-id="cbea1-128">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cbea1-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cbea1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="cbea1-129">NOTES</span></span>

## <span data-ttu-id="cbea1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cbea1-130">RELATED LINKS</span></span>

[<span data-ttu-id="cbea1-131">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cbea1-131">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="cbea1-132">Satz-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cbea1-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="cbea1-133">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cbea1-133">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


