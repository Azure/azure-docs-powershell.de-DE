---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174436"
---
# <span data-ttu-id="c82d9-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c82d9-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="c82d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c82d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c82d9-103">Abrufen des Bereitstellungsvorgangs für die Verwaltungsgruppen Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c82d9-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="c82d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c82d9-104">SYNTAX</span></span>

### <span data-ttu-id="c82d9-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c82d9-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c82d9-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c82d9-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c82d9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c82d9-107">DESCRIPTION</span></span>
<span data-ttu-id="c82d9-108">Das Cmdlet " **Get-AzManagementGroupDeploymentOperation** " listet alle Vorgänge auf, die Teil der Bereitstellung einer Verwaltungsgruppe waren, um Ihnen zu helfen, Informationen zu den genauen Vorgängen zu finden, die für eine bestimmte Bereitstellung fehlschlugen.</span><span class="sxs-lookup"><span data-stu-id="c82d9-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="c82d9-109">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c82d9-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="c82d9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c82d9-110">EXAMPLES</span></span>

### <span data-ttu-id="c82d9-111">Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="c82d9-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="c82d9-112">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="c82d9-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="c82d9-113">Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="c82d9-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="c82d9-114">Dieser Befehl ruft die Bereitstellung "Deploy01" in der Verwaltungsgruppe "myMG" ab und erhält dessen Bereitstellungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c82d9-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="c82d9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c82d9-115">PARAMETERS</span></span>

### <span data-ttu-id="c82d9-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c82d9-116">-ApiVersion</span></span>
<span data-ttu-id="c82d9-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c82d9-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c82d9-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c82d9-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c82d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c82d9-119">-DefaultProfile</span></span>
<span data-ttu-id="c82d9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c82d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c82d9-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c82d9-121">-DeploymentName</span></span>
<span data-ttu-id="c82d9-122">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="c82d9-122">The deployment name.</span></span>

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

### <span data-ttu-id="c82d9-123">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="c82d9-123">-DeploymentObject</span></span>
<span data-ttu-id="c82d9-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c82d9-124">The deployment object.</span></span>

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

### <span data-ttu-id="c82d9-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c82d9-125">-ManagementGroupId</span></span>
<span data-ttu-id="c82d9-126">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="c82d9-126">The management group id.</span></span>

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

### <span data-ttu-id="c82d9-127">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="c82d9-127">-OperationId</span></span>
<span data-ttu-id="c82d9-128">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="c82d9-128">The deployment operation Id.</span></span>

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

### <span data-ttu-id="c82d9-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="c82d9-129">-Pre</span></span>
<span data-ttu-id="c82d9-130">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c82d9-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c82d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82d9-131">CommonParameters</span></span>
<span data-ttu-id="c82d9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c82d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82d9-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c82d9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82d9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c82d9-134">INPUTS</span></span>

### <span data-ttu-id="c82d9-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c82d9-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c82d9-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c82d9-136">OUTPUTS</span></span>

### <span data-ttu-id="c82d9-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c82d9-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="c82d9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c82d9-138">NOTES</span></span>

## <span data-ttu-id="c82d9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c82d9-139">RELATED LINKS</span></span>
