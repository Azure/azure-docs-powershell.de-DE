---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844619"
---
# <span data-ttu-id="39008-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="39008-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="39008-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39008-102">SYNOPSIS</span></span>
<span data-ttu-id="39008-103">Ruft die Einstellungen der Diagnose Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="39008-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="39008-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39008-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39008-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39008-105">DESCRIPTION</span></span>
<span data-ttu-id="39008-106">Das Cmdlet " **Get-AzVMDiagnosticsExtension** " Ruft die Einstellungen der Azure Diagnostics-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="39008-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="39008-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39008-107">EXAMPLES</span></span>

### <span data-ttu-id="39008-108">Beispiel 1: Abrufen der auf einen virtuellen Computer angewendeten Diagnose Erweiterung</span><span class="sxs-lookup"><span data-stu-id="39008-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="39008-109">Mit diesem Befehl wird die auf den virtuellen Computer mit dem Namen ContosoVM22 angewendete Diagnose Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="39008-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="39008-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39008-110">PARAMETERS</span></span>

### <span data-ttu-id="39008-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39008-111">-DefaultProfile</span></span>
<span data-ttu-id="39008-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39008-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39008-113">-Name</span><span class="sxs-lookup"><span data-stu-id="39008-113">-Name</span></span>
<span data-ttu-id="39008-114">Gibt den Namen der Diagnose Erweiterung an, für die dieses Cmdlet Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="39008-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="39008-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39008-115">-ResourceGroupName</span></span>
<span data-ttu-id="39008-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="39008-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="39008-117">-Status</span><span class="sxs-lookup"><span data-stu-id="39008-117">-Status</span></span>
<span data-ttu-id="39008-118">Gibt an, dass dieses Cmdlet den Status Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="39008-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39008-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="39008-119">-VMName</span></span>
<span data-ttu-id="39008-120">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die Diagnose Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="39008-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="39008-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39008-121">CommonParameters</span></span>
<span data-ttu-id="39008-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39008-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39008-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39008-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39008-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39008-124">INPUTS</span></span>

### <span data-ttu-id="39008-125">Keine</span><span class="sxs-lookup"><span data-stu-id="39008-125">None</span></span>
<span data-ttu-id="39008-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="39008-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39008-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39008-127">OUTPUTS</span></span>

### <span data-ttu-id="39008-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="39008-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="39008-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="39008-129">NOTES</span></span>

## <span data-ttu-id="39008-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39008-130">RELATED LINKS</span></span>

[<span data-ttu-id="39008-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="39008-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="39008-132">Satz-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="39008-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


