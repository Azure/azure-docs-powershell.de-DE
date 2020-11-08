---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176977"
---
# <span data-ttu-id="a5443-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a5443-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="a5443-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5443-102">SYNOPSIS</span></span>
<span data-ttu-id="a5443-103">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a5443-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a5443-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5443-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5443-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5443-105">DESCRIPTION</span></span>
<span data-ttu-id="a5443-106">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a5443-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a5443-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5443-107">EXAMPLES</span></span>

### <span data-ttu-id="a5443-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5443-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a5443-109">Mit diesem Befehl wird ein fortlaufendes paralleles Upgrade des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a5443-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="a5443-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5443-110">PARAMETERS</span></span>

### <span data-ttu-id="a5443-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5443-111">-AsJob</span></span>
<span data-ttu-id="a5443-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a5443-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5443-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5443-113">-DefaultProfile</span></span>
<span data-ttu-id="a5443-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5443-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5443-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5443-115">-Force</span></span>
<span data-ttu-id="a5443-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a5443-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5443-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5443-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5443-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5443-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5443-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a5443-119">-VMScaleSetName</span></span>
<span data-ttu-id="a5443-120">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a5443-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="a5443-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5443-121">-Confirm</span></span>
<span data-ttu-id="a5443-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5443-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5443-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5443-123">-WhatIf</span></span>
<span data-ttu-id="a5443-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5443-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5443-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5443-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5443-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5443-126">CommonParameters</span></span>
<span data-ttu-id="a5443-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5443-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5443-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5443-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5443-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5443-129">INPUTS</span></span>

### <span data-ttu-id="a5443-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5443-130">System.String</span></span>

## <span data-ttu-id="a5443-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5443-131">OUTPUTS</span></span>

### <span data-ttu-id="a5443-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a5443-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a5443-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5443-133">NOTES</span></span>

## <span data-ttu-id="a5443-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5443-134">RELATED LINKS</span></span>
