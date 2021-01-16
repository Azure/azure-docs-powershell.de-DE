---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300960"
---
# <span data-ttu-id="384e0-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="384e0-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="384e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="384e0-102">SYNOPSIS</span></span>
<span data-ttu-id="384e0-103">Startet ein manuelles Upgrade der VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="384e0-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="384e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="384e0-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="384e0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="384e0-105">DESCRIPTION</span></span>
<span data-ttu-id="384e0-106">Das Update-AzVmssInstance cmdlet startet ein manuelles Upgrade der angegebenen Instanz des Virtual Machine Scale Set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="384e0-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="384e0-107">Dies wird verwendet, wenn die Upgraderichtlinie für den VMSS Scale Set auf manuell festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="384e0-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="384e0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="384e0-108">EXAMPLES</span></span>

### <span data-ttu-id="384e0-109">Beispiel 1: Starten eines Upgrades der VmSS-Instanz</span><span class="sxs-lookup"><span data-stu-id="384e0-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="384e0-110">Dieser Befehl startet ein Upgrade der VMSS namens VMScaleSet001 mit der Instanz-ID 0.</span><span class="sxs-lookup"><span data-stu-id="384e0-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="384e0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="384e0-111">PARAMETERS</span></span>

### <span data-ttu-id="384e0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="384e0-112">-AsJob</span></span>
<span data-ttu-id="384e0-113">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="384e0-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="384e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384e0-114">-DefaultProfile</span></span>
<span data-ttu-id="384e0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="384e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384e0-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="384e0-116">-InstanceId</span></span>
<span data-ttu-id="384e0-117">Gibt als Zeichenfolgenarray die ID oder IDs der zu aktualisierenden Instanz an.</span><span class="sxs-lookup"><span data-stu-id="384e0-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="384e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="384e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="384e0-119">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="384e0-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="384e0-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="384e0-120">-VMScaleSetName</span></span>
<span data-ttu-id="384e0-121">Gibt den Namen der VMSS-Instanz an, die dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="384e0-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="384e0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="384e0-122">-Confirm</span></span>
<span data-ttu-id="384e0-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="384e0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="384e0-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="384e0-124">-WhatIf</span></span>
<span data-ttu-id="384e0-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="384e0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="384e0-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="384e0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="384e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384e0-127">CommonParameters</span></span>
<span data-ttu-id="384e0-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="384e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384e0-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="384e0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384e0-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="384e0-130">INPUTS</span></span>

### <span data-ttu-id="384e0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="384e0-131">System.String</span></span>

### <span data-ttu-id="384e0-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="384e0-132">System.String[]</span></span>

## <span data-ttu-id="384e0-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="384e0-133">OUTPUTS</span></span>

### <span data-ttu-id="384e0-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="384e0-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="384e0-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="384e0-135">NOTES</span></span>

## <span data-ttu-id="384e0-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="384e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="384e0-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="384e0-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


