---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176009"
---
# <span data-ttu-id="ecb75-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="ecb75-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="ecb75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb75-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb75-103">Ruft die verfügbaren SKUs für die VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="ecb75-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="ecb75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecb75-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb75-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecb75-105">DESCRIPTION</span></span>
<span data-ttu-id="ecb75-106">Das **Cmdlet "Get-AzVmssSku"** ruft die verfügbaren SKUs für den Virtual Machine Scale Set (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="ecb75-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ecb75-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ecb75-107">EXAMPLES</span></span>

### <span data-ttu-id="ecb75-108">Beispiel 1: Alle verfügbaren SKUs von der VMSS erhalten</span><span class="sxs-lookup"><span data-stu-id="ecb75-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ecb75-109">Dieser Befehl ruft alle verfügbaren SKUs aus der VMSS namens ContosoVMSS ab, die zur Ressourcengruppe "ContosoGroup" gehört.</span><span class="sxs-lookup"><span data-stu-id="ecb75-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ecb75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecb75-110">PARAMETERS</span></span>

### <span data-ttu-id="ecb75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb75-111">-DefaultProfile</span></span>
<span data-ttu-id="ecb75-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ecb75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecb75-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb75-113">-ResourceGroupName</span></span>
<span data-ttu-id="ecb75-114">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="ecb75-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ecb75-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ecb75-115">-VMScaleSetName</span></span>
<span data-ttu-id="ecb75-116">Arten des Namens der VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecb75-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb75-117">CommonParameters</span></span>
<span data-ttu-id="ecb75-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb75-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecb75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb75-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ecb75-120">INPUTS</span></span>

### <span data-ttu-id="ecb75-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ecb75-121">System.String</span></span>

## <span data-ttu-id="ecb75-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ecb75-122">OUTPUTS</span></span>

### <span data-ttu-id="ecb75-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="ecb75-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="ecb75-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ecb75-124">NOTES</span></span>

## <span data-ttu-id="ecb75-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ecb75-125">RELATED LINKS</span></span>

[<span data-ttu-id="ecb75-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ecb75-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


