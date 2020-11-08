---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009304"
---
# <span data-ttu-id="6ccce-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ccce-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="6ccce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ccce-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccce-103">Startet ein paralleles Upgrade, um alle Scale-Instanzen von virtuellen Computern auf die neueste verfügbare Platt Form Abbild-Betriebssystemversion zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6ccce-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="6ccce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ccce-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ccce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ccce-105">DESCRIPTION</span></span>
<span data-ttu-id="6ccce-106">Startet ein paralleles Upgrade, um alle Scale-Instanzen von virtuellen Computern auf die neueste verfügbare Platt Form Abbild-Betriebssystemversion zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6ccce-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="6ccce-107">Instanzen, die bereits die neueste verfügbare Betriebssystemversion ausführen, sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="6ccce-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="6ccce-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ccce-108">EXAMPLES</span></span>

### <span data-ttu-id="6ccce-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ccce-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="6ccce-110">Mit diesem Befehl wird ein paralleles Upgrade aller VM-Instanzen des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="6ccce-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="6ccce-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ccce-111">PARAMETERS</span></span>

### <span data-ttu-id="6ccce-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ccce-112">-AsJob</span></span>
<span data-ttu-id="6ccce-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6ccce-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ccce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccce-114">-DefaultProfile</span></span>
<span data-ttu-id="6ccce-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ccce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ccce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccce-116">-ResourceGroupName</span></span>
<span data-ttu-id="6ccce-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ccce-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ccce-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6ccce-118">-VMScaleSetName</span></span>
<span data-ttu-id="6ccce-119">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6ccce-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="6ccce-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ccce-120">-Confirm</span></span>
<span data-ttu-id="6ccce-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ccce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ccce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ccce-122">-WhatIf</span></span>
<span data-ttu-id="6ccce-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ccce-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ccce-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ccce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ccce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccce-125">CommonParameters</span></span>
<span data-ttu-id="6ccce-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ccce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccce-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ccce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccce-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ccce-128">INPUTS</span></span>

### <span data-ttu-id="6ccce-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6ccce-129">System.String</span></span>

## <span data-ttu-id="6ccce-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ccce-130">OUTPUTS</span></span>

### <span data-ttu-id="6ccce-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6ccce-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6ccce-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ccce-132">NOTES</span></span>

## <span data-ttu-id="6ccce-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ccce-133">RELATED LINKS</span></span>
