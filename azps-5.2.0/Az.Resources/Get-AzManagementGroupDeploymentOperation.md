---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368667"
---
# <span data-ttu-id="991a8-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="991a8-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="991a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="991a8-102">SYNOPSIS</span></span>
<span data-ttu-id="991a8-103">Bereitstellungsvorgang für die Bereitstellung der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="991a8-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="991a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="991a8-104">SYNTAX</span></span>

### <span data-ttu-id="991a8-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="991a8-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="991a8-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="991a8-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="991a8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="991a8-107">DESCRIPTION</span></span>
<span data-ttu-id="991a8-108">Das **Cmdlet "Get-AzManagementGroupDeploymentOperation"** listet alle Vorgänge auf, die Teil einer Bereitstellung einer Verwaltungsgruppe waren, um Sie bei der Identifizierung und Bereitstellung genauerer Informationen zu genauen Vorgängen zu unterstützen, die bei einer bestimmten Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="991a8-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="991a8-109">Dies sind die gleichen Informationen, die in den Bereitstellungsdetails auf dem Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="991a8-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="991a8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="991a8-110">EXAMPLES</span></span>

### <span data-ttu-id="991a8-111">Beispiel 1: Bereitstellungsvorgänge mit einem Bereitstellungsnamen erhalten</span><span class="sxs-lookup"><span data-stu-id="991a8-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="991a8-112">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="991a8-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="991a8-113">Beispiel 2: Erhalten einer Bereitstellung und deren Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="991a8-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="991a8-114">Dieser Befehl ruft die Bereitstellung "Deploy01" bei der Verwaltungsgruppe "myMG" ab und ruft deren Bereitstellungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="991a8-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="991a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="991a8-115">PARAMETERS</span></span>

### <span data-ttu-id="991a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="991a8-116">-DefaultProfile</span></span>
<span data-ttu-id="991a8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="991a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="991a8-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="991a8-118">-DeploymentName</span></span>
<span data-ttu-id="991a8-119">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="991a8-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="991a8-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="991a8-120">-DeploymentObject</span></span>
<span data-ttu-id="991a8-121">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="991a8-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="991a8-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="991a8-122">-ManagementGroupId</span></span>
<span data-ttu-id="991a8-123">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="991a8-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="991a8-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="991a8-124">-OperationId</span></span>
<span data-ttu-id="991a8-125">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="991a8-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="991a8-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="991a8-126">-Pre</span></span>
<span data-ttu-id="991a8-127">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="991a8-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="991a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="991a8-128">CommonParameters</span></span>
<span data-ttu-id="991a8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="991a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="991a8-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="991a8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="991a8-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="991a8-131">INPUTS</span></span>

### <span data-ttu-id="991a8-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="991a8-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="991a8-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="991a8-133">OUTPUTS</span></span>

### <span data-ttu-id="991a8-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEploymentOperation</span><span class="sxs-lookup"><span data-stu-id="991a8-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="991a8-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="991a8-135">NOTES</span></span>

## <span data-ttu-id="991a8-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="991a8-136">RELATED LINKS</span></span>
