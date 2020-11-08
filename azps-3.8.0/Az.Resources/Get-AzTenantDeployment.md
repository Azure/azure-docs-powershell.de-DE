---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003984"
---
# <span data-ttu-id="337c9-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="337c9-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="337c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="337c9-102">SYNOPSIS</span></span>
<span data-ttu-id="337c9-103">Abrufen der Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="337c9-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="337c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="337c9-104">SYNTAX</span></span>

### <span data-ttu-id="337c9-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="337c9-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="337c9-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="337c9-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="337c9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="337c9-107">DESCRIPTION</span></span>
<span data-ttu-id="337c9-108">Mit dem Cmdlet **Get-AzTenantDeployment werden** die Bereitstellungen im MANDANTENBEREICH abgerufen.</span><span class="sxs-lookup"><span data-stu-id="337c9-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="337c9-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="337c9-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="337c9-110">Standardmäßig ruft **Get-AzTenantDeployment** alle Bereitstellungen im MANDANTENBEREICH ab.</span><span class="sxs-lookup"><span data-stu-id="337c9-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="337c9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="337c9-111">EXAMPLES</span></span>

### <span data-ttu-id="337c9-112">Beispiel 1: Abrufen aller Bereitstellungen im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="337c9-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="337c9-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen MANDANTENBEREICH ab.</span><span class="sxs-lookup"><span data-stu-id="337c9-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="337c9-114">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="337c9-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="337c9-115">Mit diesem Befehl wird die "Deploy01"-Bereitstellung im aktuellen MANDANTENBEREICH abgerufen.</span><span class="sxs-lookup"><span data-stu-id="337c9-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="337c9-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzTenantDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="337c9-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="337c9-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="337c9-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="337c9-118">Beispiel 3: Abrufen einer Bereitstellung nach ID</span><span class="sxs-lookup"><span data-stu-id="337c9-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="337c9-119">Mit diesem Befehl wird die "Deploy01"-Bereitstellung im MANDANTENBEREICH abgerufen.</span><span class="sxs-lookup"><span data-stu-id="337c9-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="337c9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="337c9-120">PARAMETERS</span></span>

### <span data-ttu-id="337c9-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="337c9-121">-ApiVersion</span></span>
<span data-ttu-id="337c9-122">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="337c9-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="337c9-123">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="337c9-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337c9-124">-DefaultProfile</span></span>
<span data-ttu-id="337c9-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="337c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="337c9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="337c9-126">-Id</span></span>
<span data-ttu-id="337c9-127">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="337c9-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="337c9-128">Beispiel:/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="337c9-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337c9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="337c9-129">-Name</span></span>
<span data-ttu-id="337c9-130">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="337c9-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337c9-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="337c9-131">-Pre</span></span>
<span data-ttu-id="337c9-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="337c9-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="337c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337c9-133">CommonParameters</span></span>
<span data-ttu-id="337c9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337c9-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="337c9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337c9-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="337c9-136">INPUTS</span></span>

### <span data-ttu-id="337c9-137">Keine</span><span class="sxs-lookup"><span data-stu-id="337c9-137">None</span></span>

## <span data-ttu-id="337c9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="337c9-138">OUTPUTS</span></span>

### <span data-ttu-id="337c9-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="337c9-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="337c9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="337c9-140">NOTES</span></span>

## <span data-ttu-id="337c9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="337c9-141">RELATED LINKS</span></span>
