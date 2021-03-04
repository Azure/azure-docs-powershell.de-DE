---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 2af89bac9e748fca0719abf34bd672d2b09c3af5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926432"
---
# <span data-ttu-id="0ba0d-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0ba0d-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="0ba0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba0d-103">Abbrechen einer laufenden Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0ba0d-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="0ba0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ba0d-104">SYNTAX</span></span>

### <span data-ttu-id="0ba0d-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ba0d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ba0d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0ba0d-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ba0d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0ba0d-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ba0d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ba0d-108">DESCRIPTION</span></span>
<span data-ttu-id="0ba0d-109">Das **Cmdlet Stop-AzManagementGroupDeployment** bricht eine Bereitstellung ab, die in einer Verwaltungsgruppe gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="0ba0d-110">Um eine Bereitstellung zu beenden, muss die Bereitstellung über einen unvollständigen Bereitstellungszustand verfügen, z. B. Bereitstellung, und nicht über einen abgeschlossenen Zustand wie "Bereitgestellt" oder "Fehlgeschlagen".</span><span class="sxs-lookup"><span data-stu-id="0ba0d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0ba0d-111">Zum Erstellen einer Bereitstellung in einer Verwaltungsgruppe verwenden Sie das New-AzManagementGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="0ba0d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ba0d-112">EXAMPLES</span></span>

### <span data-ttu-id="0ba0d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ba0d-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="0ba0d-114">Mit diesem Befehl wird die laufende Bereitstellung "deployment01" in der Verwaltungsgruppe "myMG" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="0ba0d-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ba0d-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="0ba0d-116">Dieser Befehl ruft die Bereitstellung "deployment01" bei der Verwaltungsgruppe "myMG" ab und bricht sie ab.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="0ba0d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ba0d-117">PARAMETERS</span></span>

### <span data-ttu-id="0ba0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba0d-118">-DefaultProfile</span></span>
<span data-ttu-id="0ba0d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba0d-120">-ID</span><span class="sxs-lookup"><span data-stu-id="0ba0d-120">-Id</span></span>
<span data-ttu-id="0ba0d-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0ba0d-122">Beispiel: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0ba0d-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ba0d-123">-InputObject</span></span>
<span data-ttu-id="0ba0d-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0d-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0ba0d-125">-ManagementGroupId</span></span>
<span data-ttu-id="0ba0d-126">Die Id der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0ba0d-127">-Name</span></span>
<span data-ttu-id="0ba0d-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ba0d-129">-PassThru</span></span>
<span data-ttu-id="0ba0d-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0ba0d-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0ba0d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="0ba0d-131">-Pre</span></span>
<span data-ttu-id="0ba0d-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0ba0d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ba0d-133">-Confirm</span></span>
<span data-ttu-id="0ba0d-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ba0d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ba0d-135">-WhatIf</span></span>
<span data-ttu-id="0ba0d-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ba0d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ba0d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba0d-138">CommonParameters</span></span>
<span data-ttu-id="0ba0d-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba0d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba0d-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ba0d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba0d-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ba0d-141">INPUTS</span></span>

### <span data-ttu-id="0ba0d-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="0ba0d-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0ba0d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ba0d-143">OUTPUTS</span></span>

### <span data-ttu-id="0ba0d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ba0d-144">System.Boolean</span></span>

## <span data-ttu-id="0ba0d-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0ba0d-145">NOTES</span></span>

## <span data-ttu-id="0ba0d-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0ba0d-146">RELATED LINKS</span></span>
