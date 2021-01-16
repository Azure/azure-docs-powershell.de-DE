---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295444"
---
# <span data-ttu-id="74bc8-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="74bc8-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="74bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="74bc8-103">Zeigt den Status des aktuellen Rollupgrades für den Skalierungssatz des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="74bc8-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="74bc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74bc8-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74bc8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="74bc8-106">Zeigt den Status des aktuellen Rollupgrades für den Skalierungssatz des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="74bc8-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="74bc8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="74bc8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74bc8-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="74bc8-109">Dieser Befehl zeigt den Status des letzten Rollupgrades der VMSS namens VMSS001 an, die zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="74bc8-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="74bc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74bc8-110">PARAMETERS</span></span>

### <span data-ttu-id="74bc8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bc8-111">-DefaultProfile</span></span>
<span data-ttu-id="74bc8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74bc8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74bc8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74bc8-113">-ResourceGroupName</span></span>
<span data-ttu-id="74bc8-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74bc8-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="74bc8-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="74bc8-115">-VMScaleSetName</span></span>
<span data-ttu-id="74bc8-116">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="74bc8-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="74bc8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bc8-117">CommonParameters</span></span>
<span data-ttu-id="74bc8-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74bc8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bc8-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74bc8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bc8-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74bc8-120">INPUTS</span></span>

### <span data-ttu-id="74bc8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="74bc8-121">System.String</span></span>

## <span data-ttu-id="74bc8-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74bc8-122">OUTPUTS</span></span>

### <span data-ttu-id="74bc8-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="74bc8-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="74bc8-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74bc8-124">NOTES</span></span>

## <span data-ttu-id="74bc8-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74bc8-125">RELATED LINKS</span></span>
