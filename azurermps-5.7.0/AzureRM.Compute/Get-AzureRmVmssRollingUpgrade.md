---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef9d1ac2e5bca51ee1addf8fdffd87c5045d23eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664680"
---
# <span data-ttu-id="91100-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="91100-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="91100-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91100-102">SYNOPSIS</span></span>
<span data-ttu-id="91100-103">Zeigt den Status des neuesten Skalierungs Satzes für virtuelle Maschinen mit parallelem Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="91100-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91100-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91100-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91100-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91100-105">DESCRIPTION</span></span>
<span data-ttu-id="91100-106">Zeigt den Status des neuesten Skalierungs Satzes für virtuelle Maschinen mit parallelem Upgrade an.</span><span class="sxs-lookup"><span data-stu-id="91100-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="91100-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91100-107">EXAMPLES</span></span>

### <span data-ttu-id="91100-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91100-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="91100-109">Dieser Befehl zeigt den Status des neuesten parallelen Upgrades des VMSS mit dem Namen VMSS001, das zur Ressourcengruppe namens Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="91100-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="91100-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91100-110">PARAMETERS</span></span>

### <span data-ttu-id="91100-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91100-111">-DefaultProfile</span></span>
<span data-ttu-id="91100-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91100-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91100-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91100-113">-ResourceGroupName</span></span>
<span data-ttu-id="91100-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91100-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="91100-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="91100-115">-VMScaleSetName</span></span>
<span data-ttu-id="91100-116">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="91100-116">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91100-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91100-117">CommonParameters</span></span>
<span data-ttu-id="91100-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91100-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91100-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91100-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91100-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91100-120">INPUTS</span></span>

### <span data-ttu-id="91100-121">System. String</span><span class="sxs-lookup"><span data-stu-id="91100-121">System.String</span></span>

## <span data-ttu-id="91100-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91100-122">OUTPUTS</span></span>

### <span data-ttu-id="91100-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="91100-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="91100-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="91100-124">NOTES</span></span>

## <span data-ttu-id="91100-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91100-125">RELATED LINKS</span></span>
