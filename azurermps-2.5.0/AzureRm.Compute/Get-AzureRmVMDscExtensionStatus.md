---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848335"
---
# <span data-ttu-id="8c3a6-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="8c3a6-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="8c3a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3a6-103">Ruft den Status des DSC-Erweiterungs Handlers für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c3a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c3a6-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c3a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c3a6-106">Das Cmdlet " **Get-AzureRmVMDscExtensionStatus** " Ruft den Status des Erweiterungs Handlers für die gewünschte Zustands Konfiguration (DSC) für einen virtuellen Computer in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="8c3a6-107">Wenn eine Konfiguration angewendet wird, erzeugt dieses Cmdlet eine Ausgabe, die mit dem Start-DscConfiguration-Cmdlet konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="8c3a6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c3a6-108">EXAMPLES</span></span>

### <span data-ttu-id="8c3a6-109">1:</span><span class="sxs-lookup"><span data-stu-id="8c3a6-109">1:</span></span>
```

```

## <span data-ttu-id="8c3a6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c3a6-110">PARAMETERS</span></span>

### <span data-ttu-id="8c3a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3a6-111">-DefaultProfile</span></span>
<span data-ttu-id="8c3a6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c3a6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8c3a6-113">-Name</span></span>
<span data-ttu-id="8c3a6-114">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="8c3a6-115">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzureRmVMDscExtensionStatus** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="8c3a6-116">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Satz-Cmdlet geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c3a6-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8c3a6-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="8c3a6-119">-VMName</span></span>
<span data-ttu-id="8c3a6-120">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet den Status der DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3a6-121">CommonParameters</span></span>
<span data-ttu-id="8c3a6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3a6-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3a6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3a6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c3a6-124">INPUTS</span></span>

### <span data-ttu-id="8c3a6-125">Keine</span><span class="sxs-lookup"><span data-stu-id="8c3a6-125">None</span></span>
<span data-ttu-id="8c3a6-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8c3a6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c3a6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c3a6-127">OUTPUTS</span></span>

### <span data-ttu-id="8c3a6-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="8c3a6-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="8c3a6-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c3a6-129">NOTES</span></span>

## <span data-ttu-id="8c3a6-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c3a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="8c3a6-131">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8c3a6-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


