---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995187"
---
# <span data-ttu-id="603b3-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="603b3-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="603b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="603b3-102">SYNOPSIS</span></span>
<span data-ttu-id="603b3-103">Zeigt den Status des neuesten Skalierungs Satzes für virtuelle Maschinen mit parallelem Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="603b3-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="603b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="603b3-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="603b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="603b3-105">DESCRIPTION</span></span>
<span data-ttu-id="603b3-106">Zeigt den Status des neuesten Skalierungs Satzes für virtuelle Maschinen mit parallelem Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="603b3-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="603b3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="603b3-107">EXAMPLES</span></span>

### <span data-ttu-id="603b3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="603b3-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="603b3-109">Dieser Befehl zeigt den Status des neuesten parallelen Upgrades des VMSS mit dem Namen VMSS001, das zur Ressourcengruppe namens Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="603b3-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="603b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="603b3-110">PARAMETERS</span></span>

### <span data-ttu-id="603b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603b3-111">-DefaultProfile</span></span>
<span data-ttu-id="603b3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="603b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="603b3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603b3-113">-ResourceGroupName</span></span>
<span data-ttu-id="603b3-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="603b3-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="603b3-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="603b3-115">-VMScaleSetName</span></span>
<span data-ttu-id="603b3-116">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="603b3-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="603b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603b3-117">CommonParameters</span></span>
<span data-ttu-id="603b3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="603b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603b3-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="603b3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603b3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="603b3-120">INPUTS</span></span>

### <span data-ttu-id="603b3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="603b3-121">System.String</span></span>

## <span data-ttu-id="603b3-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="603b3-122">OUTPUTS</span></span>

### <span data-ttu-id="603b3-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="603b3-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="603b3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="603b3-124">NOTES</span></span>

## <span data-ttu-id="603b3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="603b3-125">RELATED LINKS</span></span>
