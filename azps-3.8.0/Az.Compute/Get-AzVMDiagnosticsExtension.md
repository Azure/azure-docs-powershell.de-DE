---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bd56d9e76ffc71d75de0a29fa40291cb405e57fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005258"
---
# <span data-ttu-id="a14cf-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a14cf-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a14cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a14cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a14cf-103">Ruft die Einstellungen der Diagnose Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a14cf-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a14cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a14cf-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a14cf-105">DESCRIPTION</span></span>
<span data-ttu-id="a14cf-106">Das Cmdlet " **Get-AzVMDiagnosticsExtension** " Ruft die Einstellungen der Azure Diagnostics-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a14cf-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a14cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a14cf-107">EXAMPLES</span></span>

### <span data-ttu-id="a14cf-108">Beispiel 1: Abrufen der auf einen virtuellen Computer angewendeten Diagnose Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a14cf-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a14cf-109">Mit diesem Befehl wird die auf den virtuellen Computer mit dem Namen ContosoVM22 angewendete Diagnose Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a14cf-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a14cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a14cf-110">PARAMETERS</span></span>

### <span data-ttu-id="a14cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14cf-111">-DefaultProfile</span></span>
<span data-ttu-id="a14cf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a14cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14cf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a14cf-113">-Name</span></span>
<span data-ttu-id="a14cf-114">Gibt den Namen der Diagnose Erweiterung an, für die dieses Cmdlet Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="a14cf-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="a14cf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14cf-115">-ResourceGroupName</span></span>
<span data-ttu-id="a14cf-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="a14cf-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a14cf-117">-Status</span><span class="sxs-lookup"><span data-stu-id="a14cf-117">-Status</span></span>
<span data-ttu-id="a14cf-118">Gibt an, dass dieses Cmdlet den Status Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="a14cf-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14cf-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a14cf-119">-VMName</span></span>
<span data-ttu-id="a14cf-120">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die Diagnose Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="a14cf-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a14cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14cf-121">CommonParameters</span></span>
<span data-ttu-id="a14cf-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14cf-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a14cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14cf-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a14cf-124">INPUTS</span></span>

### <span data-ttu-id="a14cf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a14cf-125">System.String</span></span>

### <span data-ttu-id="a14cf-126">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a14cf-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a14cf-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a14cf-127">OUTPUTS</span></span>

### <span data-ttu-id="a14cf-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a14cf-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a14cf-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a14cf-129">NOTES</span></span>

## <span data-ttu-id="a14cf-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a14cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="a14cf-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a14cf-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="a14cf-132">Satz-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a14cf-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


