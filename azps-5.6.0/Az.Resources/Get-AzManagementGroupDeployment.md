---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 73a124070dd329daff52ec5c0de16fb55ef74354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929400"
---
# <span data-ttu-id="ca01d-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ca01d-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ca01d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca01d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca01d-103">Bereitstellung bei einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ca01d-103">Get deployment at a management group</span></span>

## <span data-ttu-id="ca01d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca01d-104">SYNTAX</span></span>

### <span data-ttu-id="ca01d-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca01d-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca01d-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ca01d-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca01d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca01d-107">DESCRIPTION</span></span>
<span data-ttu-id="ca01d-108">Das **Cmdlet Get-AzManagementGroupDeployment** ruft die Bereitstellungen bei einer Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ca01d-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="ca01d-109">Geben Sie den *Parameter Name* oder *ID* an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="ca01d-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ca01d-110">Standardmäßig ruft **Get-AzManagementGroupDeployment** alle Bereitstellungen in der Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ca01d-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="ca01d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca01d-111">EXAMPLES</span></span>

### <span data-ttu-id="ca01d-112">Beispiel 1: Alle Bereitstellungen in einer Verwaltungsgruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="ca01d-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="ca01d-113">Dieser Befehl ruft alle Bereitstellungen in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="ca01d-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="ca01d-114">Beispiel 2: Erhalten einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="ca01d-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="ca01d-115">Dieser Befehl ruft die Bereitstellung "Deploy01" bei der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="ca01d-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="ca01d-116">Sie können einer Bereitstellung beim Erstellen einen Namen zuweisen, indem Sie die **Cmdlets New-AzManagementGroupDeployment** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca01d-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="ca01d-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca01d-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ca01d-118">Beispiel 3: Erhalten einer Bereitstellung nach ID</span><span class="sxs-lookup"><span data-stu-id="ca01d-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ca01d-119">Dieser Befehl ruft die Bereitstellung "Deploy01" bei der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="ca01d-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="ca01d-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ca01d-120">PARAMETERS</span></span>

### <span data-ttu-id="ca01d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca01d-121">-DefaultProfile</span></span>
<span data-ttu-id="ca01d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca01d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca01d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="ca01d-123">-Id</span></span>
<span data-ttu-id="ca01d-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ca01d-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ca01d-125">Beispiel: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ca01d-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca01d-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ca01d-126">-ManagementGroupId</span></span>
<span data-ttu-id="ca01d-127">Die Id der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ca01d-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca01d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ca01d-128">-Name</span></span>
<span data-ttu-id="ca01d-129">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ca01d-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca01d-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="ca01d-130">-Pre</span></span>
<span data-ttu-id="ca01d-131">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca01d-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ca01d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca01d-132">CommonParameters</span></span>
<span data-ttu-id="ca01d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca01d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca01d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca01d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca01d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca01d-135">INPUTS</span></span>

### <span data-ttu-id="ca01d-136">Keine</span><span class="sxs-lookup"><span data-stu-id="ca01d-136">None</span></span>

## <span data-ttu-id="ca01d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca01d-137">OUTPUTS</span></span>

### <span data-ttu-id="ca01d-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="ca01d-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ca01d-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ca01d-139">NOTES</span></span>

## <span data-ttu-id="ca01d-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ca01d-140">RELATED LINKS</span></span>
