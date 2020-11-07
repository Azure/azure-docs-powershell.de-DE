---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: fb35bac6f43ca444762ed1cbf8511d93eab10daf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820499"
---
# <span data-ttu-id="08c62-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="08c62-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="08c62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08c62-102">SYNOPSIS</span></span>
<span data-ttu-id="08c62-103">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="08c62-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="08c62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08c62-104">SYNTAX</span></span>

### <span data-ttu-id="08c62-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="08c62-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08c62-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="08c62-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08c62-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08c62-107">DESCRIPTION</span></span>
<span data-ttu-id="08c62-108">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="08c62-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="08c62-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08c62-109">EXAMPLES</span></span>

### <span data-ttu-id="08c62-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08c62-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="08c62-111">Mit diesem Befehl wird ein fortlaufendes paralleles Upgrade des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="08c62-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="08c62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08c62-112">PARAMETERS</span></span>

### <span data-ttu-id="08c62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08c62-113">-AsJob</span></span>
<span data-ttu-id="08c62-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="08c62-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08c62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c62-115">-DefaultProfile</span></span>
<span data-ttu-id="08c62-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08c62-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c62-117">-Force</span><span class="sxs-lookup"><span data-stu-id="08c62-117">-Force</span></span>
<span data-ttu-id="08c62-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="08c62-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08c62-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c62-119">-ResourceGroupName</span></span>
<span data-ttu-id="08c62-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08c62-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="08c62-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="08c62-121">-VMScaleSetName</span></span>
<span data-ttu-id="08c62-122">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="08c62-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="08c62-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08c62-123">-Confirm</span></span>
<span data-ttu-id="08c62-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08c62-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c62-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c62-125">-WhatIf</span></span>
<span data-ttu-id="08c62-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08c62-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08c62-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08c62-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c62-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c62-128">CommonParameters</span></span>
<span data-ttu-id="08c62-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c62-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c62-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c62-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c62-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08c62-131">INPUTS</span></span>

### <span data-ttu-id="08c62-132">System. String</span><span class="sxs-lookup"><span data-stu-id="08c62-132">System.String</span></span>

## <span data-ttu-id="08c62-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08c62-133">OUTPUTS</span></span>

### <span data-ttu-id="08c62-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="08c62-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="08c62-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="08c62-135">NOTES</span></span>

## <span data-ttu-id="08c62-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08c62-136">RELATED LINKS</span></span>
