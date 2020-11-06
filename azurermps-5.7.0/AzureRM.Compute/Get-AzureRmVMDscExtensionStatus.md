---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478630"
---
# <span data-ttu-id="49c8e-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="49c8e-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="49c8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="49c8e-103">Ruft den Status des DSC-Erweiterungs Handlers für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="49c8e-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49c8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49c8e-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="49c8e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="49c8e-106">Das Cmdlet " **Get-AzureRmVMDscExtensionStatus** " Ruft den Status des Erweiterungs Handlers für die gewünschte Zustands Konfiguration (DSC) für einen virtuellen Computer in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="49c8e-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="49c8e-107">Wenn eine Konfiguration angewendet wird, erzeugt dieses Cmdlet eine Ausgabe, die mit dem Start-DscConfiguration-Cmdlet konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="49c8e-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="49c8e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49c8e-108">EXAMPLES</span></span>

## <span data-ttu-id="49c8e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="49c8e-109">PARAMETERS</span></span>

### <span data-ttu-id="49c8e-110">-Name</span><span class="sxs-lookup"><span data-stu-id="49c8e-110">-Name</span></span>
<span data-ttu-id="49c8e-111">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="49c8e-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="49c8e-112">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzureRmVMDscExtensionStatus** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49c8e-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="49c8e-113">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Satz-Cmdlet geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="49c8e-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="49c8e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c8e-114">-ResourceGroupName</span></span>
<span data-ttu-id="49c8e-115">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="49c8e-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="49c8e-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="49c8e-116">-VMName</span></span>
<span data-ttu-id="49c8e-117">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet den Status der DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="49c8e-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="49c8e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c8e-118">CommonParameters</span></span>
<span data-ttu-id="49c8e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c8e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c8e-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c8e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c8e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49c8e-121">INPUTS</span></span>

### <span data-ttu-id="49c8e-122">Keine</span><span class="sxs-lookup"><span data-stu-id="49c8e-122">None</span></span>
<span data-ttu-id="49c8e-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="49c8e-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49c8e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49c8e-124">OUTPUTS</span></span>

## <span data-ttu-id="49c8e-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="49c8e-125">NOTES</span></span>

## <span data-ttu-id="49c8e-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49c8e-126">RELATED LINKS</span></span>

[<span data-ttu-id="49c8e-127">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="49c8e-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


