---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: e87c307592f4487de239245ef06a70ea084ef916
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921432"
---
# <span data-ttu-id="f7c27-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f7c27-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="f7c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7c27-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c27-103">Zeigt den Status der neuesten Skalierungssatz für virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="f7c27-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f7c27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7c27-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7c27-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7c27-105">DESCRIPTION</span></span>
<span data-ttu-id="f7c27-106">Zeigt den Status der neuesten Skalierungssatz für virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="f7c27-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f7c27-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7c27-107">EXAMPLES</span></span>

### <span data-ttu-id="f7c27-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7c27-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f7c27-109">Dieser Befehl zeigt den Status des neuesten fortlaufenden Upgrades des VMSS namens VMSS001 an, das zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="f7c27-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f7c27-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f7c27-110">PARAMETERS</span></span>

### <span data-ttu-id="f7c27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c27-111">-DefaultProfile</span></span>
<span data-ttu-id="f7c27-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7c27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7c27-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c27-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7c27-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7c27-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7c27-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f7c27-115">-VMScaleSetName</span></span>
<span data-ttu-id="f7c27-116">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="f7c27-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="f7c27-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c27-117">CommonParameters</span></span>
<span data-ttu-id="f7c27-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c27-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c27-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7c27-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c27-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7c27-120">INPUTS</span></span>

### <span data-ttu-id="f7c27-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f7c27-121">System.String</span></span>

## <span data-ttu-id="f7c27-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7c27-122">OUTPUTS</span></span>

### <span data-ttu-id="f7c27-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="f7c27-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="f7c27-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f7c27-124">NOTES</span></span>

## <span data-ttu-id="f7c27-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f7c27-125">RELATED LINKS</span></span>
