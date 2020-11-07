---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: caf6f142c9669ba3f1b5f343c4bbb1a4dc978a97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820736"
---
# <span data-ttu-id="903e9-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="903e9-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="903e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="903e9-102">SYNOPSIS</span></span>
<span data-ttu-id="903e9-103">Ruft den Status des DSC-Erweiterungs Handlers für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="903e9-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="903e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="903e9-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="903e9-105">DESCRIPTION</span></span>
<span data-ttu-id="903e9-106">Das Cmdlet " **Get-AzVMDscExtensionStatus** " Ruft den Status des Erweiterungs Handlers für die gewünschte Zustands Konfiguration (DSC) für einen virtuellen Computer in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="903e9-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="903e9-107">Wenn eine Konfiguration angewendet wird, erzeugt dieses Cmdlet eine Ausgabe, die mit dem Start-DscConfiguration-Cmdlet konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="903e9-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="903e9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="903e9-108">EXAMPLES</span></span>

## <span data-ttu-id="903e9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="903e9-109">PARAMETERS</span></span>

### <span data-ttu-id="903e9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903e9-110">-DefaultProfile</span></span>
<span data-ttu-id="903e9-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="903e9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903e9-112">-Name</span><span class="sxs-lookup"><span data-stu-id="903e9-112">-Name</span></span>
<span data-ttu-id="903e9-113">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="903e9-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="903e9-114">Mit dem Set-AzVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzVMDscExtensionStatus** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="903e9-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="903e9-115">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Satz-Cmdlet geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="903e9-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="903e9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903e9-116">-ResourceGroupName</span></span>
<span data-ttu-id="903e9-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="903e9-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="903e9-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="903e9-118">-VMName</span></span>
<span data-ttu-id="903e9-119">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet den Status der DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="903e9-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="903e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903e9-120">CommonParameters</span></span>
<span data-ttu-id="903e9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903e9-122">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="903e9-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903e9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="903e9-123">INPUTS</span></span>

### <span data-ttu-id="903e9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="903e9-124">System.String</span></span>

## <span data-ttu-id="903e9-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="903e9-125">OUTPUTS</span></span>

### <span data-ttu-id="903e9-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="903e9-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="903e9-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="903e9-127">NOTES</span></span>

## <span data-ttu-id="903e9-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="903e9-128">RELATED LINKS</span></span>

[<span data-ttu-id="903e9-129">Satz-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="903e9-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


