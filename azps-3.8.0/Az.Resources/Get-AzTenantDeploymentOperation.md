---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003983"
---
# <span data-ttu-id="dee82-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dee82-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="dee82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dee82-102">SYNOPSIS</span></span>
<span data-ttu-id="dee82-103">Abrufen des Bereitstellungsvorgangs für die Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="dee82-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="dee82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dee82-104">SYNTAX</span></span>

### <span data-ttu-id="dee82-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dee82-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dee82-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="dee82-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee82-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dee82-107">DESCRIPTION</span></span>
<span data-ttu-id="dee82-108">Das Cmdlet " **Get-AzTenantDeploymentOperation** " listet alle Vorgänge auf, die Teil der Bereitstellung im aktuellen MANDANTENBEREICH waren, um Ihnen zu helfen, weitere Informationen zu den genauen Vorgängen zu finden, die für eine bestimmte Bereitstellung fehlschlugen.</span><span class="sxs-lookup"><span data-stu-id="dee82-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="dee82-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dee82-109">EXAMPLES</span></span>

### <span data-ttu-id="dee82-110">Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="dee82-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="dee82-111">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" im aktuellen MANDANTENBEREICH ab.</span><span class="sxs-lookup"><span data-stu-id="dee82-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="dee82-112">Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="dee82-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="dee82-113">Dieser Befehl ruft die Bereitstellung "Deploy01" im aktuellen MANDANTENBEREICH ab und erhält dessen Bereitstellungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="dee82-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="dee82-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dee82-114">PARAMETERS</span></span>

### <span data-ttu-id="dee82-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dee82-115">-ApiVersion</span></span>
<span data-ttu-id="dee82-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dee82-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dee82-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dee82-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="dee82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee82-118">-DefaultProfile</span></span>
<span data-ttu-id="dee82-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dee82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee82-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="dee82-120">-DeploymentName</span></span>
<span data-ttu-id="dee82-121">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="dee82-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee82-122">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="dee82-122">-DeploymentObject</span></span>
<span data-ttu-id="dee82-123">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="dee82-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dee82-124">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="dee82-124">-OperationId</span></span>
<span data-ttu-id="dee82-125">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="dee82-125">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee82-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="dee82-126">-Pre</span></span>
<span data-ttu-id="dee82-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="dee82-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dee82-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee82-128">CommonParameters</span></span>
<span data-ttu-id="dee82-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee82-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee82-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dee82-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee82-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dee82-131">INPUTS</span></span>

### <span data-ttu-id="dee82-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="dee82-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dee82-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dee82-133">OUTPUTS</span></span>

### <span data-ttu-id="dee82-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dee82-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="dee82-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="dee82-135">NOTES</span></span>

## <span data-ttu-id="dee82-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dee82-136">RELATED LINKS</span></span>
