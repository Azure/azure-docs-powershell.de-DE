---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496637"
---
# <span data-ttu-id="29b6b-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="29b6b-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="29b6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="29b6b-103">Ruft die Einstellungen der Diagnose Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="29b6b-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29b6b-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="29b6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="29b6b-106">Das Cmdlet " **Get-AzureRmVMDiagnosticsExtension** " Ruft die Einstellungen der Azure Diagnostics-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="29b6b-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="29b6b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="29b6b-108">Beispiel 1: Abrufen der auf einen virtuellen Computer angewendeten Diagnose Erweiterung</span><span class="sxs-lookup"><span data-stu-id="29b6b-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="29b6b-109">Mit diesem Befehl wird die auf den virtuellen Computer mit dem Namen ContosoVM22 angewendete Diagnose Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="29b6b-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="29b6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29b6b-110">PARAMETERS</span></span>

### <span data-ttu-id="29b6b-111">-Name</span><span class="sxs-lookup"><span data-stu-id="29b6b-111">-Name</span></span>
<span data-ttu-id="29b6b-112">Gibt den Namen der Diagnose Erweiterung an, für die dieses Cmdlet Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="29b6b-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="29b6b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b6b-113">-ResourceGroupName</span></span>
<span data-ttu-id="29b6b-114">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="29b6b-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="29b6b-115">-Status</span><span class="sxs-lookup"><span data-stu-id="29b6b-115">-Status</span></span>
<span data-ttu-id="29b6b-116">Gibt an, dass dieses Cmdlet den Status Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="29b6b-116">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="29b6b-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="29b6b-117">-VMName</span></span>
<span data-ttu-id="29b6b-118">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die Diagnose Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="29b6b-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="29b6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b6b-119">CommonParameters</span></span>
<span data-ttu-id="29b6b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b6b-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b6b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b6b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29b6b-122">INPUTS</span></span>

### <span data-ttu-id="29b6b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="29b6b-123">None</span></span>
<span data-ttu-id="29b6b-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="29b6b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29b6b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29b6b-125">OUTPUTS</span></span>

## <span data-ttu-id="29b6b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="29b6b-126">NOTES</span></span>

## <span data-ttu-id="29b6b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29b6b-127">RELATED LINKS</span></span>

[<span data-ttu-id="29b6b-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="29b6b-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="29b6b-129">Satz-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="29b6b-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


