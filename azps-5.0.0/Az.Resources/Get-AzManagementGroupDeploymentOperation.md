---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301173"
---
# <span data-ttu-id="9c022-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9c022-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="9c022-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c022-102">SYNOPSIS</span></span>
<span data-ttu-id="9c022-103">Abrufen des Bereitstellungsvorgangs für die Verwaltungsgruppen Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9c022-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="9c022-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c022-104">SYNTAX</span></span>

### <span data-ttu-id="9c022-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c022-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c022-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9c022-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c022-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c022-107">DESCRIPTION</span></span>
<span data-ttu-id="9c022-108">Das Cmdlet " **Get-AzManagementGroupDeploymentOperation** " listet alle Vorgänge auf, die Teil der Bereitstellung einer Verwaltungsgruppe waren, um Ihnen zu helfen, Informationen zu den genauen Vorgängen zu finden, die für eine bestimmte Bereitstellung fehlschlugen.</span><span class="sxs-lookup"><span data-stu-id="9c022-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="9c022-109">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c022-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="9c022-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c022-110">EXAMPLES</span></span>

### <span data-ttu-id="9c022-111">Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="9c022-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="9c022-112">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="9c022-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="9c022-113">Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="9c022-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="9c022-114">Dieser Befehl ruft die Bereitstellung "Deploy01" in der Verwaltungsgruppe "myMG" ab und erhält dessen Bereitstellungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="9c022-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="9c022-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c022-115">PARAMETERS</span></span>

### <span data-ttu-id="9c022-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c022-116">-DefaultProfile</span></span>
<span data-ttu-id="9c022-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c022-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c022-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="9c022-118">-DeploymentName</span></span>
<span data-ttu-id="9c022-119">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="9c022-119">The deployment name.</span></span>

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

### <span data-ttu-id="9c022-120">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="9c022-120">-DeploymentObject</span></span>
<span data-ttu-id="9c022-121">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="9c022-121">The deployment object.</span></span>

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

### <span data-ttu-id="9c022-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9c022-122">-ManagementGroupId</span></span>
<span data-ttu-id="9c022-123">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="9c022-123">The management group id.</span></span>

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

### <span data-ttu-id="9c022-124">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="9c022-124">-OperationId</span></span>
<span data-ttu-id="9c022-125">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="9c022-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="9c022-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c022-126">-Pre</span></span>
<span data-ttu-id="9c022-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="9c022-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9c022-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c022-128">CommonParameters</span></span>
<span data-ttu-id="9c022-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c022-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c022-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c022-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c022-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c022-131">INPUTS</span></span>

### <span data-ttu-id="9c022-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9c022-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9c022-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c022-133">OUTPUTS</span></span>

### <span data-ttu-id="9c022-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9c022-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="9c022-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c022-135">NOTES</span></span>

## <span data-ttu-id="9c022-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c022-136">RELATED LINKS</span></span>
