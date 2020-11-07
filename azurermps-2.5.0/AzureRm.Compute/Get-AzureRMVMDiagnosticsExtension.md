---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: e02c86407326d9ea5b12a5a589e5860c9dfb5c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850947"
---
# <span data-ttu-id="80907-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="80907-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="80907-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80907-102">SYNOPSIS</span></span>
<span data-ttu-id="80907-103">Ruft die Einstellungen der Diagnose Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="80907-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80907-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80907-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80907-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80907-105">DESCRIPTION</span></span>
<span data-ttu-id="80907-106">Das Cmdlet " **Get-AzureRmVMDiagnosticsExtension** " Ruft die Einstellungen der Azure Diagnostics-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="80907-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="80907-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80907-107">EXAMPLES</span></span>

### <span data-ttu-id="80907-108">Beispiel 1: Abrufen der auf einen virtuellen Computer angewendeten Diagnose Erweiterung</span><span class="sxs-lookup"><span data-stu-id="80907-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="80907-109">Mit diesem Befehl wird die auf den virtuellen Computer mit dem Namen ContosoVM22 angewendete Diagnose Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="80907-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="80907-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80907-110">PARAMETERS</span></span>

### <span data-ttu-id="80907-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80907-111">-DefaultProfile</span></span>
<span data-ttu-id="80907-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80907-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80907-113">-Name</span><span class="sxs-lookup"><span data-stu-id="80907-113">-Name</span></span>
<span data-ttu-id="80907-114">Gibt den Namen der Diagnose Erweiterung an, für die dieses Cmdlet Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="80907-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="80907-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80907-115">-ResourceGroupName</span></span>
<span data-ttu-id="80907-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="80907-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="80907-117">-Status</span><span class="sxs-lookup"><span data-stu-id="80907-117">-Status</span></span>
<span data-ttu-id="80907-118">Gibt an, dass dieses Cmdlet den Status Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="80907-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="80907-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="80907-119">-VMName</span></span>
<span data-ttu-id="80907-120">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die Diagnose Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="80907-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="80907-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80907-121">CommonParameters</span></span>
<span data-ttu-id="80907-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80907-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80907-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80907-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80907-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80907-124">INPUTS</span></span>

### <span data-ttu-id="80907-125">Keine</span><span class="sxs-lookup"><span data-stu-id="80907-125">None</span></span>
<span data-ttu-id="80907-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="80907-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80907-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80907-127">OUTPUTS</span></span>

### <span data-ttu-id="80907-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="80907-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="80907-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="80907-129">NOTES</span></span>

## <span data-ttu-id="80907-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80907-130">RELATED LINKS</span></span>

[<span data-ttu-id="80907-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="80907-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="80907-132">Satz-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="80907-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


