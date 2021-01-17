---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308147"
---
# <span data-ttu-id="2a4ce-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2a4ce-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2a4ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4ce-103">Entfernt eine Bereitstellung für eine Verwaltungsgruppe und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="2a4ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a4ce-104">SYNTAX</span></span>

### <span data-ttu-id="2a4ce-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a4ce-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a4ce-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2a4ce-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a4ce-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a4ce-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a4ce-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a4ce-108">DESCRIPTION</span></span>
<span data-ttu-id="2a4ce-109">Das **Cmdlet "Remove-AzManagementGroupDeployment"** entfernt eine Azure-Bereitstellung für eine Verwaltungsgruppe und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="2a4ce-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a4ce-110">EXAMPLES</span></span>

### <span data-ttu-id="2a4ce-111">Beispiel 1: Entfernen einer Bereitstellung mit einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="2a4ce-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="2a4ce-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" bei der Verwaltungsgruppe "myMG" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="2a4ce-113">Beispiel 2: Erhalten und Entfernen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2a4ce-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="2a4ce-114">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" bei der Verwaltungsgruppe "myMG" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="2a4ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a4ce-115">PARAMETERS</span></span>

### <span data-ttu-id="2a4ce-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a4ce-116">-AsJob</span></span>
<span data-ttu-id="2a4ce-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2a4ce-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a4ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4ce-118">-DefaultProfile</span></span>
<span data-ttu-id="2a4ce-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4ce-120">-ID</span><span class="sxs-lookup"><span data-stu-id="2a4ce-120">-Id</span></span>
<span data-ttu-id="2a4ce-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2a4ce-122">beispiel: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2a4ce-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="2a4ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a4ce-123">-InputObject</span></span>
<span data-ttu-id="2a4ce-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-124">The deployment object.</span></span>

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

### <span data-ttu-id="2a4ce-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2a4ce-125">-ManagementGroupId</span></span>
<span data-ttu-id="2a4ce-126">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-126">The management group id.</span></span>

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

### <span data-ttu-id="2a4ce-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2a4ce-127">-Name</span></span>
<span data-ttu-id="2a4ce-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="2a4ce-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a4ce-129">-PassThru</span></span>
<span data-ttu-id="2a4ce-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2a4ce-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2a4ce-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a4ce-131">-Pre</span></span>
<span data-ttu-id="2a4ce-132">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2a4ce-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a4ce-133">-Confirm</span></span>
<span data-ttu-id="2a4ce-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a4ce-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a4ce-135">-WhatIf</span></span>
<span data-ttu-id="2a4ce-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a4ce-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a4ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4ce-138">CommonParameters</span></span>
<span data-ttu-id="2a4ce-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4ce-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a4ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4ce-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a4ce-141">INPUTS</span></span>

### <span data-ttu-id="2a4ce-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2a4ce-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2a4ce-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a4ce-143">OUTPUTS</span></span>

### <span data-ttu-id="2a4ce-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a4ce-144">System.Boolean</span></span>

## <span data-ttu-id="2a4ce-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a4ce-145">NOTES</span></span>

## <span data-ttu-id="2a4ce-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a4ce-146">RELATED LINKS</span></span>
