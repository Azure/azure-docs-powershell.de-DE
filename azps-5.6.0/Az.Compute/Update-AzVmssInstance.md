---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: ed0ad08d94cbc67832b6a0dbb85882bd18692d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939643"
---
# <span data-ttu-id="194f1-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="194f1-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="194f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="194f1-102">SYNOPSIS</span></span>
<span data-ttu-id="194f1-103">Startet ein manuelles Upgrade der VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="194f1-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="194f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="194f1-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="194f1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="194f1-105">DESCRIPTION</span></span>
<span data-ttu-id="194f1-106">Das Update-AzVmssInstance-Cmdlet startet ein manuelles Upgrade der angegebenen VMSS-Instanz (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="194f1-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="194f1-107">Dies wird verwendet, wenn die Upgraderichtlinie für den VMSS-Skalierungssatz auf manuell festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="194f1-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="194f1-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="194f1-108">EXAMPLES</span></span>

### <span data-ttu-id="194f1-109">Beispiel 1: Starten eines Upgrades der VMSS-Instanz</span><span class="sxs-lookup"><span data-stu-id="194f1-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="194f1-110">Mit diesem Befehl wird ein Upgrade des VMSS namens VMScaleSet001 gestartet, das die Instanz-ID 0 hat.</span><span class="sxs-lookup"><span data-stu-id="194f1-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="194f1-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="194f1-111">PARAMETERS</span></span>

### <span data-ttu-id="194f1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="194f1-112">-AsJob</span></span>
<span data-ttu-id="194f1-113">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="194f1-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="194f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="194f1-114">-DefaultProfile</span></span>
<span data-ttu-id="194f1-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="194f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="194f1-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="194f1-116">-InstanceId</span></span>
<span data-ttu-id="194f1-117">Gibt als Zeichenfolgenarray die ID oder IDs der zu aktualisierenden Instanz an.</span><span class="sxs-lookup"><span data-stu-id="194f1-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="194f1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="194f1-118">-ResourceGroupName</span></span>
<span data-ttu-id="194f1-119">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="194f1-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="194f1-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="194f1-120">-VMScaleSetName</span></span>
<span data-ttu-id="194f1-121">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="194f1-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="194f1-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="194f1-122">-Confirm</span></span>
<span data-ttu-id="194f1-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="194f1-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194f1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="194f1-124">-WhatIf</span></span>
<span data-ttu-id="194f1-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="194f1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="194f1-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="194f1-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194f1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194f1-127">CommonParameters</span></span>
<span data-ttu-id="194f1-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="194f1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194f1-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="194f1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194f1-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="194f1-130">INPUTS</span></span>

### <span data-ttu-id="194f1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="194f1-131">System.String</span></span>

### <span data-ttu-id="194f1-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="194f1-132">System.String[]</span></span>

## <span data-ttu-id="194f1-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="194f1-133">OUTPUTS</span></span>

### <span data-ttu-id="194f1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="194f1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="194f1-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="194f1-135">NOTES</span></span>

## <span data-ttu-id="194f1-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="194f1-136">RELATED LINKS</span></span>

[<span data-ttu-id="194f1-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="194f1-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


