---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: cbe44db07cbf32195f92ebefc0a2032a5f288a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651875"
---
# <span data-ttu-id="57552-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="57552-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="57552-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57552-102">SYNOPSIS</span></span>
<span data-ttu-id="57552-103">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="57552-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="57552-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57552-104">SYNTAX</span></span>

### <span data-ttu-id="57552-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="57552-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57552-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="57552-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57552-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57552-107">DESCRIPTION</span></span>
<span data-ttu-id="57552-108">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="57552-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="57552-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57552-109">EXAMPLES</span></span>

### <span data-ttu-id="57552-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57552-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="57552-111">Mit diesem Befehl wird ein fortlaufendes paralleles Upgrade des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="57552-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="57552-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="57552-112">PARAMETERS</span></span>

### <span data-ttu-id="57552-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57552-113">-AsJob</span></span>
<span data-ttu-id="57552-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="57552-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57552-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57552-115">-DefaultProfile</span></span>
<span data-ttu-id="57552-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57552-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57552-117">-Force</span><span class="sxs-lookup"><span data-stu-id="57552-117">-Force</span></span>
<span data-ttu-id="57552-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="57552-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57552-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57552-119">-ResourceGroupName</span></span>
<span data-ttu-id="57552-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57552-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57552-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="57552-121">-VMScaleSetName</span></span>
<span data-ttu-id="57552-122">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="57552-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57552-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57552-123">-Confirm</span></span>
<span data-ttu-id="57552-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57552-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57552-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57552-125">-WhatIf</span></span>
<span data-ttu-id="57552-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57552-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57552-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57552-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57552-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57552-128">CommonParameters</span></span>
<span data-ttu-id="57552-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57552-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57552-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57552-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57552-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57552-131">INPUTS</span></span>

### <span data-ttu-id="57552-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57552-132">System.String</span></span>

## <span data-ttu-id="57552-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57552-133">OUTPUTS</span></span>

### <span data-ttu-id="57552-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="57552-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="57552-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="57552-135">NOTES</span></span>

## <span data-ttu-id="57552-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57552-136">RELATED LINKS</span></span>
