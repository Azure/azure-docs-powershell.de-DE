---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 5bf59cb766d82e2fc50bdc75c0a072e2b8d17a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925787"
---
# <span data-ttu-id="5e112-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5e112-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="5e112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e112-102">SYNOPSIS</span></span>
<span data-ttu-id="5e112-103">Ruft den Schritt ab.</span><span class="sxs-lookup"><span data-stu-id="5e112-103">Gets the step.</span></span>

## <span data-ttu-id="5e112-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e112-104">SYNTAX</span></span>

### <span data-ttu-id="5e112-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e112-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e112-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e112-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e112-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5e112-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e112-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e112-108">DESCRIPTION</span></span>
<span data-ttu-id="5e112-109">Das **Cmdlet Get-AzDeploymentManagerStep** ruft einen Schritt ab und gibt ein -Objekt zurück, das diesen Schritt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e112-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="5e112-110">Geben Sie den Schritt nach dem Namen und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="5e112-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="5e112-111">Alternativ können Sie das Step-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e112-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="5e112-112">Sie können dieses Objekt lokal ändern und dann Änderungen auf die Artefaktquelle anwenden, indem Sie das cmdlet Set-AzDeploymentManagerStep verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e112-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="5e112-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e112-113">EXAMPLES</span></span>

### <span data-ttu-id="5e112-114">Beispiel 1: Einen Schritt erhalten</span><span class="sxs-lookup"><span data-stu-id="5e112-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="5e112-115">Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5e112-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5e112-116">Beispiel 2: Einen Schritt mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="5e112-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="5e112-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e112-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="5e112-118">Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5e112-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5e112-119">Beispiel 3: Einen Schritt mit einem von der Anwendung zurückgegebenen Objekt New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5e112-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="5e112-120">Dieser Befehl ruft einen Schritt ab, dessen Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5e112-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="5e112-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e112-121">PARAMETERS</span></span>

### <span data-ttu-id="5e112-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e112-122">-DefaultProfile</span></span>
<span data-ttu-id="5e112-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e112-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e112-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e112-124">-InputObject</span></span>
<span data-ttu-id="5e112-125">Das Schrittressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="5e112-125">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e112-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5e112-126">-Name</span></span>
<span data-ttu-id="5e112-127">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="5e112-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e112-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e112-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e112-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e112-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e112-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e112-130">-ResourceId</span></span>
<span data-ttu-id="5e112-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5e112-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e112-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e112-132">CommonParameters</span></span>
<span data-ttu-id="5e112-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e112-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e112-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e112-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e112-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e112-135">INPUTS</span></span>

### <span data-ttu-id="5e112-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5e112-136">System.String</span></span>

### <span data-ttu-id="5e112-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="5e112-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="5e112-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e112-138">OUTPUTS</span></span>

### <span data-ttu-id="5e112-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="5e112-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="5e112-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e112-140">NOTES</span></span>

## <span data-ttu-id="5e112-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e112-141">RELATED LINKS</span></span>
