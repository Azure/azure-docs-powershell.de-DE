---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 482d2d5b7dd88618bb29270f6ef3cec4e133e842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663664"
---
# <span data-ttu-id="9bfe7-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="9bfe7-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="9bfe7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfe7-103">Ruft den Status des DSC-Erweiterungs Handlers für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bfe7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bfe7-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bfe7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bfe7-105">DESCRIPTION</span></span>
<span data-ttu-id="9bfe7-106">Das Cmdlet " **Get-AzureRmVMDscExtensionStatus** " Ruft den Status des Erweiterungs Handlers für die gewünschte Zustands Konfiguration (DSC) für einen virtuellen Computer in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="9bfe7-107">Wenn eine Konfiguration angewendet wird, erzeugt dieses Cmdlet eine Ausgabe, die mit dem Start-DscConfiguration-Cmdlet konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="9bfe7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bfe7-108">EXAMPLES</span></span>

## <span data-ttu-id="9bfe7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bfe7-109">PARAMETERS</span></span>

### <span data-ttu-id="9bfe7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfe7-110">-DefaultProfile</span></span>
<span data-ttu-id="9bfe7-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bfe7-112">-Name</span><span class="sxs-lookup"><span data-stu-id="9bfe7-112">-Name</span></span>
<span data-ttu-id="9bfe7-113">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9bfe7-114">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzureRmVMDscExtensionStatus** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="9bfe7-115">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Satz-Cmdlet geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfe7-116">-ResourceGroupName</span></span>
<span data-ttu-id="9bfe7-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9bfe7-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="9bfe7-118">-VMName</span></span>
<span data-ttu-id="9bfe7-119">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet den Status der DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfe7-120">CommonParameters</span></span>
<span data-ttu-id="9bfe7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfe7-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfe7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfe7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bfe7-123">INPUTS</span></span>

### <span data-ttu-id="9bfe7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9bfe7-124">System.String</span></span>

## <span data-ttu-id="9bfe7-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bfe7-125">OUTPUTS</span></span>

### <span data-ttu-id="9bfe7-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="9bfe7-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="9bfe7-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bfe7-127">NOTES</span></span>

## <span data-ttu-id="9bfe7-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bfe7-128">RELATED LINKS</span></span>

[<span data-ttu-id="9bfe7-129">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9bfe7-129">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


