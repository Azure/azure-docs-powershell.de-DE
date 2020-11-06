---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 292da4caf90fb43895ec5cda12dcfc6418e6bde9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503818"
---
# <span data-ttu-id="2888c-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2888c-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="2888c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2888c-102">SYNOPSIS</span></span>
<span data-ttu-id="2888c-103">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2888c-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2888c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2888c-104">SYNTAX</span></span>

### <span data-ttu-id="2888c-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="2888c-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2888c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2888c-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2888c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2888c-107">DESCRIPTION</span></span>
<span data-ttu-id="2888c-108">Bricht den aktuellen Skalierungs Satz für den virtuellen Computer auf, um das parallele Upgrade auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2888c-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="2888c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2888c-109">EXAMPLES</span></span>

### <span data-ttu-id="2888c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2888c-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="2888c-111">Mit diesem Befehl wird ein fortlaufendes paralleles Upgrade des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2888c-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="2888c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2888c-112">PARAMETERS</span></span>

### <span data-ttu-id="2888c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2888c-113">-AsJob</span></span>
<span data-ttu-id="2888c-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2888c-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2888c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2888c-115">-DefaultProfile</span></span>
<span data-ttu-id="2888c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2888c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2888c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2888c-117">-Force</span></span>
<span data-ttu-id="2888c-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2888c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2888c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2888c-119">-ResourceGroupName</span></span>
<span data-ttu-id="2888c-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2888c-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888c-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2888c-121">-VMScaleSetName</span></span>
<span data-ttu-id="2888c-122">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2888c-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2888c-123">-Confirm</span></span>
<span data-ttu-id="2888c-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2888c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2888c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2888c-125">-WhatIf</span></span>
<span data-ttu-id="2888c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2888c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2888c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2888c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2888c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2888c-128">CommonParameters</span></span>
<span data-ttu-id="2888c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2888c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2888c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2888c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2888c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2888c-131">INPUTS</span></span>

### <span data-ttu-id="2888c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2888c-132">System.String</span></span>

## <span data-ttu-id="2888c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2888c-133">OUTPUTS</span></span>

### <span data-ttu-id="2888c-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2888c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2888c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2888c-135">NOTES</span></span>

## <span data-ttu-id="2888c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2888c-136">RELATED LINKS</span></span>
