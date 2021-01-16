---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307659"
---
# <span data-ttu-id="58d07-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="58d07-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="58d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d07-102">SYNOPSIS</span></span>
<span data-ttu-id="58d07-103">Entfernt eine Bereitstellung im Mandantenbereich und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="58d07-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="58d07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58d07-104">SYNTAX</span></span>

### <span data-ttu-id="58d07-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="58d07-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d07-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="58d07-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d07-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="58d07-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d07-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58d07-108">DESCRIPTION</span></span>
<span data-ttu-id="58d07-109">Das **Cmdlet "Remove-AzTenantDeployment"** entfernt eine Azure-Bereitstellung im aktuellen Mandantenbereich und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="58d07-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="58d07-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58d07-110">EXAMPLES</span></span>

### <span data-ttu-id="58d07-111">Beispiel 1: Entfernen einer Bereitstellung mit einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="58d07-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="58d07-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Mandantenbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="58d07-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="58d07-113">Beispiel 2: Erhalten und Entfernen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="58d07-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="58d07-114">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Mandantenbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="58d07-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="58d07-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58d07-115">PARAMETERS</span></span>

### <span data-ttu-id="58d07-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58d07-116">-AsJob</span></span>
<span data-ttu-id="58d07-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="58d07-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58d07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d07-118">-DefaultProfile</span></span>
<span data-ttu-id="58d07-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58d07-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d07-120">-ID</span><span class="sxs-lookup"><span data-stu-id="58d07-120">-Id</span></span>
<span data-ttu-id="58d07-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="58d07-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="58d07-122">beispiel: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="58d07-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="58d07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58d07-123">-InputObject</span></span>
<span data-ttu-id="58d07-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="58d07-124">The deployment object.</span></span>

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

### <span data-ttu-id="58d07-125">-Name</span><span class="sxs-lookup"><span data-stu-id="58d07-125">-Name</span></span>
<span data-ttu-id="58d07-126">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="58d07-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d07-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58d07-127">-PassThru</span></span>
<span data-ttu-id="58d07-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="58d07-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="58d07-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="58d07-129">-Pre</span></span>
<span data-ttu-id="58d07-130">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58d07-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="58d07-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58d07-131">-Confirm</span></span>
<span data-ttu-id="58d07-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58d07-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d07-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58d07-133">-WhatIf</span></span>
<span data-ttu-id="58d07-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58d07-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d07-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58d07-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d07-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d07-136">CommonParameters</span></span>
<span data-ttu-id="58d07-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d07-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d07-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58d07-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d07-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58d07-139">INPUTS</span></span>

### <span data-ttu-id="58d07-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="58d07-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="58d07-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58d07-141">OUTPUTS</span></span>

### <span data-ttu-id="58d07-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58d07-142">System.Boolean</span></span>

## <span data-ttu-id="58d07-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58d07-143">NOTES</span></span>

## <span data-ttu-id="58d07-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58d07-144">RELATED LINKS</span></span>
