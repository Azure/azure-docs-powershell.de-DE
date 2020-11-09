---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301185"
---
# <span data-ttu-id="99d62-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="99d62-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="99d62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99d62-102">SYNOPSIS</span></span>
<span data-ttu-id="99d62-103">Abrufen der Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="99d62-103">Get deployment at a management group</span></span>

## <span data-ttu-id="99d62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99d62-104">SYNTAX</span></span>

### <span data-ttu-id="99d62-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="99d62-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d62-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="99d62-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99d62-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99d62-107">DESCRIPTION</span></span>
<span data-ttu-id="99d62-108">Das Cmdlet " **Get-AzManagementGroupDeployment** " Ruft die Bereitstellungen in der a-Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="99d62-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="99d62-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="99d62-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="99d62-110">Standardmäßig ruft **Get-AzManagementGroupDeployment** alle Bereitstellungen in der Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="99d62-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="99d62-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99d62-111">EXAMPLES</span></span>

### <span data-ttu-id="99d62-112">Beispiel 1: Abrufen aller Bereitstellungen in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="99d62-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="99d62-113">Dieser Befehl ruft alle Bereitstellungen in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="99d62-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="99d62-114">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="99d62-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="99d62-115">Dieser Befehl ruft die "Deploy01"-Bereitstellung in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="99d62-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="99d62-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzManagementGroupDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="99d62-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="99d62-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="99d62-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="99d62-118">Beispiel 3: Abrufen einer Bereitstellung nach ID</span><span class="sxs-lookup"><span data-stu-id="99d62-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="99d62-119">Dieser Befehl ruft die "Deploy01"-Bereitstellung in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="99d62-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="99d62-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="99d62-120">PARAMETERS</span></span>

### <span data-ttu-id="99d62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d62-121">-DefaultProfile</span></span>
<span data-ttu-id="99d62-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99d62-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d62-123">-ID</span><span class="sxs-lookup"><span data-stu-id="99d62-123">-Id</span></span>
<span data-ttu-id="99d62-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="99d62-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="99d62-125">Beispiel:/Providers/Microsoft.Management/managementGroups/{managementGroupId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="99d62-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="99d62-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="99d62-126">-ManagementGroupId</span></span>
<span data-ttu-id="99d62-127">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="99d62-127">The management group id.</span></span>

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

### <span data-ttu-id="99d62-128">-Name</span><span class="sxs-lookup"><span data-stu-id="99d62-128">-Name</span></span>
<span data-ttu-id="99d62-129">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="99d62-129">The name of deployment.</span></span>

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

### <span data-ttu-id="99d62-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="99d62-130">-Pre</span></span>
<span data-ttu-id="99d62-131">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="99d62-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="99d62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d62-132">CommonParameters</span></span>
<span data-ttu-id="99d62-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d62-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99d62-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d62-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99d62-135">INPUTS</span></span>

### <span data-ttu-id="99d62-136">Keine</span><span class="sxs-lookup"><span data-stu-id="99d62-136">None</span></span>

## <span data-ttu-id="99d62-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99d62-137">OUTPUTS</span></span>

### <span data-ttu-id="99d62-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="99d62-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="99d62-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="99d62-139">NOTES</span></span>

## <span data-ttu-id="99d62-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99d62-140">RELATED LINKS</span></span>
