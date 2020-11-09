---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301059"
---
# <span data-ttu-id="c9160-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="c9160-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="c9160-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9160-102">SYNOPSIS</span></span>
<span data-ttu-id="c9160-103">Abrufen der Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="c9160-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="c9160-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9160-104">SYNTAX</span></span>

### <span data-ttu-id="c9160-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9160-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9160-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c9160-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9160-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9160-107">DESCRIPTION</span></span>
<span data-ttu-id="c9160-108">Mit dem Cmdlet **Get-AzTenantDeployment werden** die Bereitstellungen im MANDANTENBEREICH abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c9160-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="c9160-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c9160-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="c9160-110">Standardmäßig ruft **Get-AzTenantDeployment** alle Bereitstellungen im MANDANTENBEREICH ab.</span><span class="sxs-lookup"><span data-stu-id="c9160-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="c9160-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9160-111">EXAMPLES</span></span>

### <span data-ttu-id="c9160-112">Beispiel 1: Abrufen aller Bereitstellungen im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="c9160-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="c9160-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen MANDANTENBEREICH ab.</span><span class="sxs-lookup"><span data-stu-id="c9160-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="c9160-114">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="c9160-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="c9160-115">Mit diesem Befehl wird die "Deploy01"-Bereitstellung im aktuellen MANDANTENBEREICH abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c9160-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="c9160-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzTenantDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9160-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="c9160-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9160-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="c9160-118">Beispiel 3: Abrufen einer Bereitstellung nach ID</span><span class="sxs-lookup"><span data-stu-id="c9160-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="c9160-119">Mit diesem Befehl wird die "Deploy01"-Bereitstellung im MANDANTENBEREICH abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c9160-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="c9160-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9160-120">PARAMETERS</span></span>

### <span data-ttu-id="c9160-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9160-121">-DefaultProfile</span></span>
<span data-ttu-id="c9160-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9160-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9160-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c9160-123">-Id</span></span>
<span data-ttu-id="c9160-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c9160-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c9160-125">Beispiel:/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c9160-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c9160-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c9160-126">-Name</span></span>
<span data-ttu-id="c9160-127">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c9160-127">The name of deployment.</span></span>

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

### <span data-ttu-id="c9160-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="c9160-128">-Pre</span></span>
<span data-ttu-id="c9160-129">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c9160-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c9160-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9160-130">CommonParameters</span></span>
<span data-ttu-id="c9160-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9160-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9160-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9160-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9160-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9160-133">INPUTS</span></span>

### <span data-ttu-id="c9160-134">Keine</span><span class="sxs-lookup"><span data-stu-id="c9160-134">None</span></span>

## <span data-ttu-id="c9160-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9160-135">OUTPUTS</span></span>

### <span data-ttu-id="c9160-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c9160-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c9160-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9160-137">NOTES</span></span>

## <span data-ttu-id="c9160-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9160-138">RELATED LINKS</span></span>
