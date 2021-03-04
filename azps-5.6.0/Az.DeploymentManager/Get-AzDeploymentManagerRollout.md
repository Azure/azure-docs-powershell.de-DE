---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: 53458d53dd6d8b3f698dc51fc6b1463c9a9134e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925795"
---
# <span data-ttu-id="6c5fd-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6c5fd-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="6c5fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5fd-103">Ruft das Rollout ab.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-103">Gets the rollout.</span></span>

## <span data-ttu-id="6c5fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c5fd-104">SYNTAX</span></span>

### <span data-ttu-id="6c5fd-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c5fd-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c5fd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c5fd-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c5fd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c5fd-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c5fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c5fd-108">DESCRIPTION</span></span>
<span data-ttu-id="6c5fd-109">Das **Get-AzDeploymentManagerRollout-Cmdlet** ruft ein Rollout ab und gibt ein -Objekt zurück, das dieses Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="6c5fd-110">Geben Sie das Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="6c5fd-111">Alternativ können Sie das Rolloutobjekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="6c5fd-112">Das zurückgegebene Rolloutobjekt enthält die Dienste, Diensteinheiten und Schritte, die bereitgestellt wurden und die in Bearbeitung sind.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="6c5fd-113">Diejenigen, die noch bereitgestellt werden müssen, befinden sich nicht in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="6c5fd-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c5fd-114">EXAMPLES</span></span>

### <span data-ttu-id="6c5fd-115">Beispiel 1 Rollout</span><span class="sxs-lookup"><span data-stu-id="6c5fd-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="6c5fd-116">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="6c5fd-117">Beispiel 2 : Informationen zum Rollout erhalten und anzeigen</span><span class="sxs-lookup"><span data-stu-id="6c5fd-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="6c5fd-118">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="6c5fd-119">Der Schalter -Verbose zeigt alle Rolloutdetails hierarchisch an. zeigt die Dienste, die ServiceUnits und die Schritte unter den einzelnen ServiceUnit- und Kontextinformationen für jeden Schritt für eine holistische Ansicht des Rollouts an.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="6c5fd-120">Beispiel 3: Rollout mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="6c5fd-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="6c5fd-121">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6c5fd-122">Beispiel 4: Ein Rollout mithilfe des Rolloutobjekts.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="6c5fd-123">Dieser Befehl ruft ein Rollout ab, dessen Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="6c5fd-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6c5fd-124">PARAMETERS</span></span>

### <span data-ttu-id="6c5fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5fd-125">-DefaultProfile</span></span>
<span data-ttu-id="6c5fd-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c5fd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c5fd-127">-InputObject</span></span>
<span data-ttu-id="6c5fd-128">Rolloutobjekt.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-128">Rollout object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5fd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6c5fd-129">-Name</span></span>
<span data-ttu-id="6c5fd-130">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="6c5fd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c5fd-131">-ResourceGroupName</span></span>
<span data-ttu-id="6c5fd-132">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-132">The resource group.</span></span>

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

### <span data-ttu-id="6c5fd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c5fd-133">-ResourceId</span></span>
<span data-ttu-id="6c5fd-134">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-134">The resource identifier.</span></span>

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

### <span data-ttu-id="6c5fd-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="6c5fd-135">-RetryAttempt</span></span>
<span data-ttu-id="6c5fd-136">Der Wiederholungsversuch des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5fd-137">CommonParameters</span></span>
<span data-ttu-id="6c5fd-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5fd-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c5fd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5fd-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c5fd-140">INPUTS</span></span>

### <span data-ttu-id="6c5fd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6c5fd-141">System.String</span></span>

### <span data-ttu-id="6c5fd-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6c5fd-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6c5fd-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="6c5fd-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="6c5fd-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c5fd-144">OUTPUTS</span></span>

### <span data-ttu-id="6c5fd-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="6c5fd-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="6c5fd-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6c5fd-146">NOTES</span></span>

## <span data-ttu-id="6c5fd-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6c5fd-147">RELATED LINKS</span></span>
