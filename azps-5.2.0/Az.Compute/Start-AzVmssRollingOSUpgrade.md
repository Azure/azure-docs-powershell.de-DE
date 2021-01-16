---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291592"
---
# <span data-ttu-id="048e2-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="048e2-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="048e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="048e2-102">SYNOPSIS</span></span>
<span data-ttu-id="048e2-103">Startet ein rollübergreifendes Upgrade, um alle Skalierungssatzinstanzen für virtuelle Computer auf die neueste verfügbare Version des Betriebssystems für Plattformimages zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="048e2-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="048e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="048e2-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="048e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="048e2-105">DESCRIPTION</span></span>
<span data-ttu-id="048e2-106">Startet ein rollübergreifendes Upgrade, um alle Skalierungssatzinstanzen für virtuelle Computer auf die neueste verfügbare Version des Betriebssystems für Plattformimages zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="048e2-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="048e2-107">Instanzen, auf denen bereits die neueste verfügbare Betriebssystemversion ausgeführt wird, sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="048e2-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="048e2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="048e2-108">EXAMPLES</span></span>

### <span data-ttu-id="048e2-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="048e2-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="048e2-110">Dieser Befehl startet ein rolliertes Upgrade aller vm-Instanzen des VM-Skalierungs-Set "VMSS001" in der Ressourcengruppe "Group001".</span><span class="sxs-lookup"><span data-stu-id="048e2-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="048e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="048e2-111">PARAMETERS</span></span>

### <span data-ttu-id="048e2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="048e2-112">-AsJob</span></span>
<span data-ttu-id="048e2-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="048e2-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048e2-114">-DefaultProfile</span></span>
<span data-ttu-id="048e2-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="048e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="048e2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048e2-116">-ResourceGroupName</span></span>
<span data-ttu-id="048e2-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="048e2-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="048e2-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="048e2-118">-VMScaleSetName</span></span>
<span data-ttu-id="048e2-119">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="048e2-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="048e2-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="048e2-120">-Confirm</span></span>
<span data-ttu-id="048e2-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="048e2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048e2-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="048e2-122">-WhatIf</span></span>
<span data-ttu-id="048e2-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="048e2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="048e2-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="048e2-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048e2-125">CommonParameters</span></span>
<span data-ttu-id="048e2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048e2-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="048e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048e2-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="048e2-128">INPUTS</span></span>

### <span data-ttu-id="048e2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="048e2-129">System.String</span></span>

## <span data-ttu-id="048e2-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="048e2-130">OUTPUTS</span></span>

### <span data-ttu-id="048e2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="048e2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="048e2-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="048e2-132">NOTES</span></span>

## <span data-ttu-id="048e2-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="048e2-133">RELATED LINKS</span></span>
