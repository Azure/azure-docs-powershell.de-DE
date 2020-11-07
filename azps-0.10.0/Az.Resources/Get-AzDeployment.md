---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: d47660d5867c1d7f9fad04884ba66c9e2c996900
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843459"
---
# <span data-ttu-id="d4934-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d4934-101">Get-AzDeployment</span></span>

## <span data-ttu-id="d4934-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4934-102">SYNOPSIS</span></span>
<span data-ttu-id="d4934-103">Bereitstellung abrufen</span><span class="sxs-lookup"><span data-stu-id="d4934-103">Get deployment</span></span>

## <span data-ttu-id="d4934-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4934-104">SYNTAX</span></span>

### <span data-ttu-id="d4934-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4934-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4934-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d4934-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4934-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4934-107">DESCRIPTION</span></span>
<span data-ttu-id="d4934-108">Mit dem Cmdlet **Get-AzDeployment werden** die Bereitstellungen im aktuellen Abonnement Bereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d4934-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="d4934-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d4934-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d4934-110">Standardmäßig ruft **Get-AzDeployment** alle Bereitstellungen im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="d4934-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="d4934-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4934-111">EXAMPLES</span></span>

### <span data-ttu-id="d4934-112">Beispiel 1: Abrufen aller Bereitstellungen im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="d4934-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="d4934-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="d4934-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="d4934-114">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="d4934-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="d4934-115">Mit diesem Befehl wird die DeployRoles01-Bereitstellung im aktuellen Abonnement Bereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d4934-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="d4934-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4934-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="d4934-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4934-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="d4934-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4934-118">PARAMETERS</span></span>

### <span data-ttu-id="d4934-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4934-119">-ApiVersion</span></span>
<span data-ttu-id="d4934-120">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4934-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d4934-121">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d4934-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d4934-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4934-122">-DefaultProfile</span></span>
<span data-ttu-id="d4934-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4934-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4934-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d4934-124">-Id</span></span>
<span data-ttu-id="d4934-125">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d4934-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d4934-126">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d4934-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4934-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d4934-127">-Name</span></span>
<span data-ttu-id="d4934-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d4934-128">The name of deployment.</span></span>

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

### <span data-ttu-id="d4934-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4934-129">-Pre</span></span>
<span data-ttu-id="d4934-130">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d4934-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d4934-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4934-131">CommonParameters</span></span>
<span data-ttu-id="d4934-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4934-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4934-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4934-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4934-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4934-134">INPUTS</span></span>

### <span data-ttu-id="d4934-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d4934-135">System.String</span></span>

## <span data-ttu-id="d4934-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4934-136">OUTPUTS</span></span>

### <span data-ttu-id="d4934-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d4934-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d4934-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4934-138">NOTES</span></span>

## <span data-ttu-id="d4934-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4934-139">RELATED LINKS</span></span>
