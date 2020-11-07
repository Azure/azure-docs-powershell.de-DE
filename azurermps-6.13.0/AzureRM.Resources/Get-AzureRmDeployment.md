---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
ms.openlocfilehash: 6d25bcf98adb740ec695152eb5b27ec9402082c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662790"
---
# <span data-ttu-id="c93e3-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c93e3-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="c93e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c93e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c93e3-103">Bereitstellung abrufen</span><span class="sxs-lookup"><span data-stu-id="c93e3-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c93e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c93e3-104">SYNTAX</span></span>

### <span data-ttu-id="c93e3-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c93e3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c93e3-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c93e3-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c93e3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c93e3-107">DESCRIPTION</span></span>
<span data-ttu-id="c93e3-108">Mit dem Cmdlet **Get-AzureRmDeployment werden** die Bereitstellungen im aktuellen Abonnement Bereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c93e3-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="c93e3-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c93e3-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="c93e3-110">Standardmäßig ruft **Get-AzureRmDeployment** alle Bereitstellungen im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c93e3-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="c93e3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c93e3-111">EXAMPLES</span></span>

### <span data-ttu-id="c93e3-112">Beispiel 1: Abrufen aller Bereitstellungen im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="c93e3-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="c93e3-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c93e3-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="c93e3-114">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="c93e3-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="c93e3-115">Mit diesem Befehl wird die DeployRoles01-Bereitstellung im aktuellen Abonnement Bereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c93e3-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="c93e3-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzureRmDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="c93e3-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="c93e3-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c93e3-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="c93e3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c93e3-118">PARAMETERS</span></span>

### <span data-ttu-id="c93e3-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c93e3-119">-ApiVersion</span></span>
<span data-ttu-id="c93e3-120">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c93e3-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c93e3-121">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c93e3-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c93e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93e3-122">-DefaultProfile</span></span>
<span data-ttu-id="c93e3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c93e3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93e3-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c93e3-124">-Id</span></span>
<span data-ttu-id="c93e3-125">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c93e3-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c93e3-126">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c93e3-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c93e3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c93e3-127">-Name</span></span>
<span data-ttu-id="c93e3-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c93e3-128">The name of deployment.</span></span>

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

### <span data-ttu-id="c93e3-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="c93e3-129">-Pre</span></span>
<span data-ttu-id="c93e3-130">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c93e3-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c93e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93e3-131">CommonParameters</span></span>
<span data-ttu-id="c93e3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93e3-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93e3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93e3-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c93e3-134">INPUTS</span></span>

### <span data-ttu-id="c93e3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c93e3-135">System.String</span></span>

## <span data-ttu-id="c93e3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c93e3-136">OUTPUTS</span></span>

### <span data-ttu-id="c93e3-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c93e3-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c93e3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c93e3-138">NOTES</span></span>

## <span data-ttu-id="c93e3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c93e3-139">RELATED LINKS</span></span>
