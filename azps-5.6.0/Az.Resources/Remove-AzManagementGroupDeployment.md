---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: 06f3dec483c2c8b5e1730cb1046f927d6d38a7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926459"
---
# <span data-ttu-id="ffa51-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffa51-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ffa51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa51-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa51-103">Entfernt eine Bereitstellung in einer Verwaltungsgruppe und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ffa51-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="ffa51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffa51-104">SYNTAX</span></span>

### <span data-ttu-id="ffa51-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffa51-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa51-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ffa51-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa51-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ffa51-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa51-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffa51-108">DESCRIPTION</span></span>
<span data-ttu-id="ffa51-109">Das **Cmdlet Remove-AzManagementGroupDeployment** entfernt eine Azure-Bereitstellung bei einer Verwaltungsgruppe und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ffa51-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="ffa51-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffa51-110">EXAMPLES</span></span>

### <span data-ttu-id="ffa51-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="ffa51-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="ffa51-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ffa51-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="ffa51-113">Beispiel 2: Eine Bereitstellung erhalten und entfernen</span><span class="sxs-lookup"><span data-stu-id="ffa51-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="ffa51-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG" ab und entfernt sie.</span><span class="sxs-lookup"><span data-stu-id="ffa51-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="ffa51-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ffa51-115">PARAMETERS</span></span>

### <span data-ttu-id="ffa51-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa51-116">-AsJob</span></span>
<span data-ttu-id="ffa51-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ffa51-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffa51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa51-118">-DefaultProfile</span></span>
<span data-ttu-id="ffa51-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffa51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa51-120">-ID</span><span class="sxs-lookup"><span data-stu-id="ffa51-120">-Id</span></span>
<span data-ttu-id="ffa51-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ffa51-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ffa51-122">Beispiel: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ffa51-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffa51-123">-InputObject</span></span>
<span data-ttu-id="ffa51-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ffa51-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ffa51-125">-ManagementGroupId</span></span>
<span data-ttu-id="ffa51-126">Die Id der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ffa51-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ffa51-127">-Name</span></span>
<span data-ttu-id="ffa51-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ffa51-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffa51-129">-PassThru</span></span>
<span data-ttu-id="ffa51-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ffa51-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ffa51-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ffa51-131">-Pre</span></span>
<span data-ttu-id="ffa51-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffa51-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ffa51-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffa51-133">-Confirm</span></span>
<span data-ttu-id="ffa51-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffa51-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa51-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa51-135">-WhatIf</span></span>
<span data-ttu-id="ffa51-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffa51-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa51-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffa51-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa51-138">CommonParameters</span></span>
<span data-ttu-id="ffa51-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa51-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa51-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa51-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffa51-141">INPUTS</span></span>

### <span data-ttu-id="ffa51-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="ffa51-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ffa51-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffa51-143">OUTPUTS</span></span>

### <span data-ttu-id="ffa51-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ffa51-144">System.Boolean</span></span>

## <span data-ttu-id="ffa51-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ffa51-145">NOTES</span></span>

## <span data-ttu-id="ffa51-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ffa51-146">RELATED LINKS</span></span>
