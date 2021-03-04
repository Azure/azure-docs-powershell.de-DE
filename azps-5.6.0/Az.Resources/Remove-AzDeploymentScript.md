---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 813291fd0014665958dbee85be36060801b3e569
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930848"
---
# <span data-ttu-id="a2253-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a2253-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="a2253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2253-102">SYNOPSIS</span></span>
<span data-ttu-id="a2253-103">Entfernt ein Bereitstellungsskript und die zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a2253-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="a2253-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2253-104">SYNTAX</span></span>

### <span data-ttu-id="a2253-105">RemoveDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2253-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2253-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2253-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2253-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2253-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2253-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2253-108">DESCRIPTION</span></span>
<span data-ttu-id="a2253-109">Das **Cmdlet Remove-AzDeploymentScript** entfernt ein Bereitstellungsskript und die zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a2253-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="a2253-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2253-110">EXAMPLES</span></span>

### <span data-ttu-id="a2253-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2253-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="a2253-112">Löscht ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a2253-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="a2253-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a2253-113">PARAMETERS</span></span>

### <span data-ttu-id="a2253-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2253-114">-Confirm</span></span>
<span data-ttu-id="a2253-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2253-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2253-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2253-116">-DefaultProfile</span></span>
<span data-ttu-id="a2253-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2253-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2253-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a2253-118">-Id</span></span>
<span data-ttu-id="a2253-119">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="a2253-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="a2253-120">Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="a2253-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2253-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2253-121">-InputObject</span></span>
<span data-ttu-id="a2253-122">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="a2253-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2253-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a2253-123">-Name</span></span>
<span data-ttu-id="a2253-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2253-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2253-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2253-125">-PassThru</span></span>
<span data-ttu-id="a2253-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a2253-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a2253-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2253-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2253-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2253-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2253-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2253-129">-WhatIf</span></span>
<span data-ttu-id="a2253-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2253-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2253-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2253-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2253-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2253-132">CommonParameters</span></span>
<span data-ttu-id="a2253-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2253-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a2253-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2253-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2253-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2253-135">INPUTS</span></span>

### <span data-ttu-id="a2253-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a2253-136">System.String</span></span>

### <span data-ttu-id="a2253-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a2253-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a2253-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2253-138">OUTPUTS</span></span>

### <span data-ttu-id="a2253-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a2253-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a2253-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a2253-140">NOTES</span></span>

## <span data-ttu-id="a2253-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a2253-141">RELATED LINKS</span></span>