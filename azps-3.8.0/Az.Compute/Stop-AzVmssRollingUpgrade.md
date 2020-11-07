---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846143"
---
# <span data-ttu-id="17072-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="17072-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="17072-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17072-102">SYNOPSIS</span></span>
<span data-ttu-id="17072-103">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="17072-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="17072-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17072-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17072-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17072-105">DESCRIPTION</span></span>
<span data-ttu-id="17072-106">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="17072-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="17072-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17072-107">EXAMPLES</span></span>

### <span data-ttu-id="17072-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17072-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="17072-109">Mit diesem Befehl wird ein fortlaufendes paralleles Upgrade des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="17072-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="17072-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="17072-110">PARAMETERS</span></span>

### <span data-ttu-id="17072-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17072-111">-AsJob</span></span>
<span data-ttu-id="17072-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17072-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17072-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17072-113">-DefaultProfile</span></span>
<span data-ttu-id="17072-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17072-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17072-115">-Force</span><span class="sxs-lookup"><span data-stu-id="17072-115">-Force</span></span>
<span data-ttu-id="17072-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="17072-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17072-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17072-117">-ResourceGroupName</span></span>
<span data-ttu-id="17072-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17072-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="17072-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="17072-119">-VMScaleSetName</span></span>
<span data-ttu-id="17072-120">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="17072-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="17072-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17072-121">-Confirm</span></span>
<span data-ttu-id="17072-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17072-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17072-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17072-123">-WhatIf</span></span>
<span data-ttu-id="17072-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17072-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17072-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17072-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17072-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17072-126">CommonParameters</span></span>
<span data-ttu-id="17072-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17072-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17072-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17072-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17072-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17072-129">INPUTS</span></span>

### <span data-ttu-id="17072-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17072-130">System.String</span></span>

## <span data-ttu-id="17072-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17072-131">OUTPUTS</span></span>

### <span data-ttu-id="17072-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="17072-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="17072-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="17072-133">NOTES</span></span>

## <span data-ttu-id="17072-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17072-134">RELATED LINKS</span></span>
