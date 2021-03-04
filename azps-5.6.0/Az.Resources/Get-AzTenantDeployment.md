---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: 1755438dfc5bdb9b4eedf46ec364e851a2bca154
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942144"
---
# <span data-ttu-id="147b1-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="147b1-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="147b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="147b1-102">SYNOPSIS</span></span>
<span data-ttu-id="147b1-103">Bereitstellung im Mandantenbereich</span><span class="sxs-lookup"><span data-stu-id="147b1-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="147b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="147b1-104">SYNTAX</span></span>

### <span data-ttu-id="147b1-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="147b1-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="147b1-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="147b1-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="147b1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="147b1-107">DESCRIPTION</span></span>
<span data-ttu-id="147b1-108">Das **Cmdlet Get-AzTenantDeployment** ruft die Bereitstellungen im Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="147b1-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="147b1-109">Geben Sie den *Parameter Name* oder *ID* an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="147b1-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="147b1-110">Standardmäßig ruft **Get-AzTenantDeployment** alle Bereitstellungen im Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="147b1-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="147b1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="147b1-111">EXAMPLES</span></span>

### <span data-ttu-id="147b1-112">Beispiel 1: Alle Bereitstellungen im Mandantenbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="147b1-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="147b1-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="147b1-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="147b1-114">Beispiel 2: Erhalten einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="147b1-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="147b1-115">Dieser Befehl ruft die Bereitstellung "Deploy01" im aktuellen Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="147b1-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="147b1-116">Sie können einer Bereitstellung beim Erstellen einen Namen zuweisen, indem Sie die **Cmdlets New-AzTenantDeployment** verwenden.</span><span class="sxs-lookup"><span data-stu-id="147b1-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="147b1-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="147b1-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="147b1-118">Beispiel 3: Erhalten einer Bereitstellung nach ID</span><span class="sxs-lookup"><span data-stu-id="147b1-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="147b1-119">Dieser Befehl ruft die Bereitstellung "Deploy01" im Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="147b1-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="147b1-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="147b1-120">PARAMETERS</span></span>

### <span data-ttu-id="147b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147b1-121">-DefaultProfile</span></span>
<span data-ttu-id="147b1-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="147b1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="147b1-123">-ID</span><span class="sxs-lookup"><span data-stu-id="147b1-123">-Id</span></span>
<span data-ttu-id="147b1-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="147b1-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="147b1-125">Beispiel: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="147b1-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="147b1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="147b1-126">-Name</span></span>
<span data-ttu-id="147b1-127">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="147b1-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b1-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="147b1-128">-Pre</span></span>
<span data-ttu-id="147b1-129">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="147b1-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="147b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147b1-130">CommonParameters</span></span>
<span data-ttu-id="147b1-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="147b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147b1-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="147b1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147b1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="147b1-133">INPUTS</span></span>

### <span data-ttu-id="147b1-134">Keine</span><span class="sxs-lookup"><span data-stu-id="147b1-134">None</span></span>

## <span data-ttu-id="147b1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="147b1-135">OUTPUTS</span></span>

### <span data-ttu-id="147b1-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="147b1-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="147b1-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="147b1-137">NOTES</span></span>

## <span data-ttu-id="147b1-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="147b1-138">RELATED LINKS</span></span>
