---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932315"
---
# <span data-ttu-id="9e747-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="9e747-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="9e747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e747-102">SYNOPSIS</span></span>
<span data-ttu-id="9e747-103">Entfernt eine Bereitstellung im Mandantenbereich und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9e747-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="9e747-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e747-104">SYNTAX</span></span>

### <span data-ttu-id="9e747-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e747-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e747-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9e747-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e747-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e747-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e747-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e747-108">DESCRIPTION</span></span>
<span data-ttu-id="9e747-109">Das **Cmdlet Remove-AzTenantDeployment** entfernt eine Azure-Bereitstellung im aktuellen Mandantenbereich und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9e747-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="9e747-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e747-110">EXAMPLES</span></span>

### <span data-ttu-id="9e747-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="9e747-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="9e747-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Mandantenbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="9e747-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="9e747-113">Beispiel 2: Eine Bereitstellung erhalten und entfernen</span><span class="sxs-lookup"><span data-stu-id="9e747-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="9e747-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Mandantenbereich ab und entfernt sie.</span><span class="sxs-lookup"><span data-stu-id="9e747-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="9e747-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e747-115">PARAMETERS</span></span>

### <span data-ttu-id="9e747-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e747-116">-AsJob</span></span>
<span data-ttu-id="9e747-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9e747-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e747-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e747-118">-DefaultProfile</span></span>
<span data-ttu-id="9e747-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e747-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e747-120">-ID</span><span class="sxs-lookup"><span data-stu-id="9e747-120">-Id</span></span>
<span data-ttu-id="9e747-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="9e747-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="9e747-122">Beispiel: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="9e747-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="9e747-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e747-123">-InputObject</span></span>
<span data-ttu-id="9e747-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="9e747-124">The deployment object.</span></span>

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

### <span data-ttu-id="9e747-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9e747-125">-Name</span></span>
<span data-ttu-id="9e747-126">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="9e747-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="9e747-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e747-127">-PassThru</span></span>
<span data-ttu-id="9e747-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="9e747-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9e747-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="9e747-129">-Pre</span></span>
<span data-ttu-id="9e747-130">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e747-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9e747-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e747-131">-Confirm</span></span>
<span data-ttu-id="9e747-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e747-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e747-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e747-133">-WhatIf</span></span>
<span data-ttu-id="9e747-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e747-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e747-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e747-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e747-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e747-136">CommonParameters</span></span>
<span data-ttu-id="9e747-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e747-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e747-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e747-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e747-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e747-139">INPUTS</span></span>

### <span data-ttu-id="9e747-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="9e747-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9e747-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e747-141">OUTPUTS</span></span>

### <span data-ttu-id="9e747-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e747-142">System.Boolean</span></span>

## <span data-ttu-id="9e747-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e747-143">NOTES</span></span>

## <span data-ttu-id="9e747-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e747-144">RELATED LINKS</span></span>
