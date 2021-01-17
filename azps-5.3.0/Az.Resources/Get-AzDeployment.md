---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459492"
---
# <span data-ttu-id="1039c-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1039c-101">Get-AzDeployment</span></span>

## <span data-ttu-id="1039c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1039c-102">SYNOPSIS</span></span>
<span data-ttu-id="1039c-103">Bereitstellung erhalten</span><span class="sxs-lookup"><span data-stu-id="1039c-103">Get deployment</span></span>

## <span data-ttu-id="1039c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1039c-104">SYNTAX</span></span>

### <span data-ttu-id="1039c-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1039c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1039c-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1039c-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1039c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1039c-107">DESCRIPTION</span></span>
<span data-ttu-id="1039c-108">Das **Cmdlet "Get-AzDeployment"** ruft die Bereitstellungen im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="1039c-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="1039c-109">Geben Sie den *Parameter "Name"* oder *"ID"* an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="1039c-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="1039c-110">Standardmäßig ruft **"Get-AzDeployment"** alle Bereitstellungen im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="1039c-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="1039c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1039c-111">EXAMPLES</span></span>

### <span data-ttu-id="1039c-112">Beispiel 1: Alle Bereitstellungen im Abonnementbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="1039c-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="1039c-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="1039c-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="1039c-114">Beispiel 2: Benennen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1039c-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="1039c-115">Dieser Befehl ruft die Bereitstellung "DeployRoles01" im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="1039c-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="1039c-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie sie mithilfe der **Cmdlets "New-AzDeployment"** erstellen.</span><span class="sxs-lookup"><span data-stu-id="1039c-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="1039c-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1039c-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="1039c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1039c-118">PARAMETERS</span></span>

### <span data-ttu-id="1039c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1039c-119">-DefaultProfile</span></span>
<span data-ttu-id="1039c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1039c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1039c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1039c-121">-Id</span></span>
<span data-ttu-id="1039c-122">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="1039c-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="1039c-123">Beispiel: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="1039c-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="1039c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1039c-124">-Name</span></span>
<span data-ttu-id="1039c-125">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="1039c-125">The name of deployment.</span></span>

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

### <span data-ttu-id="1039c-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="1039c-126">-Pre</span></span>
<span data-ttu-id="1039c-127">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1039c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1039c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1039c-128">CommonParameters</span></span>
<span data-ttu-id="1039c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1039c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1039c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1039c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1039c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1039c-131">INPUTS</span></span>

### <span data-ttu-id="1039c-132">Keine</span><span class="sxs-lookup"><span data-stu-id="1039c-132">None</span></span>

## <span data-ttu-id="1039c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1039c-133">OUTPUTS</span></span>

### <span data-ttu-id="1039c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1039c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1039c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1039c-135">NOTES</span></span>

## <span data-ttu-id="1039c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1039c-136">RELATED LINKS</span></span>
