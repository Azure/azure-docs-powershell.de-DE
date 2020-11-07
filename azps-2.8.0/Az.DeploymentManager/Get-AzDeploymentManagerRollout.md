---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651372"
---
# <span data-ttu-id="026cf-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="026cf-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="026cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="026cf-102">SYNOPSIS</span></span>
<span data-ttu-id="026cf-103">Ruft den Rollout ab.</span><span class="sxs-lookup"><span data-stu-id="026cf-103">Gets the rollout.</span></span>

## <span data-ttu-id="026cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="026cf-104">SYNTAX</span></span>

### <span data-ttu-id="026cf-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="026cf-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="026cf-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="026cf-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="026cf-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="026cf-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="026cf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="026cf-108">DESCRIPTION</span></span>
<span data-ttu-id="026cf-109">Das Cmdlet " **Get-AzDeploymentManagerRollout** " Ruft ein Rollout ab und gibt ein Objekt zurück, das diesen Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="026cf-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="026cf-110">Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="026cf-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="026cf-111">Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="026cf-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="026cf-112">Das zurückgegebene Rollout-Objekt enthält die Dienste, Dienst Einheiten und Schritte, die bereitgestellt wurden und die in Bearbeitung sind.</span><span class="sxs-lookup"><span data-stu-id="026cf-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="026cf-113">Diejenigen, die noch bereitgestellt werden, sind nicht in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="026cf-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="026cf-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="026cf-114">EXAMPLES</span></span>

### <span data-ttu-id="026cf-115">Beispiel 1 Abrufen des Rollouts</span><span class="sxs-lookup"><span data-stu-id="026cf-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="026cf-116">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="026cf-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="026cf-117">Beispiel 2 Abrufen und Anzeigen der Rollout Details</span><span class="sxs-lookup"><span data-stu-id="026cf-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="026cf-118">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="026cf-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="026cf-119">Der-verbose-Schalter zeigt alle Rollout-Details hierarchisch an; zeigt die Dienste, die ServiceUnits und die Schritte unter den einzelnen Serviceunit sowie Kontextinformationen für die einzelnen Schritte für eine ganzheitliche Ansicht des Rollouts an.</span><span class="sxs-lookup"><span data-stu-id="026cf-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="026cf-120">Beispiel 3: Abrufen eines Rollouts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="026cf-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="026cf-121">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="026cf-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="026cf-122">Beispiel 4: Abrufen eines Rollouts mithilfe des Rollout-Objekts.</span><span class="sxs-lookup"><span data-stu-id="026cf-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="026cf-123">Dieser Befehl ruft ein Rollout ab, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="026cf-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="026cf-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="026cf-124">PARAMETERS</span></span>

### <span data-ttu-id="026cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026cf-125">-DefaultProfile</span></span>
<span data-ttu-id="026cf-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="026cf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="026cf-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="026cf-127">-InputObject</span></span>
<span data-ttu-id="026cf-128">Rollout-Objekt.</span><span class="sxs-lookup"><span data-stu-id="026cf-128">Rollout object.</span></span>

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

### <span data-ttu-id="026cf-129">-Name</span><span class="sxs-lookup"><span data-stu-id="026cf-129">-Name</span></span>
<span data-ttu-id="026cf-130">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="026cf-130">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026cf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026cf-131">-ResourceGroupName</span></span>
<span data-ttu-id="026cf-132">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="026cf-132">The resource group.</span></span>

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

### <span data-ttu-id="026cf-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="026cf-133">-ResourceId</span></span>
<span data-ttu-id="026cf-134">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="026cf-134">The resource identifier.</span></span>

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

### <span data-ttu-id="026cf-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="026cf-135">-RetryAttempt</span></span>
<span data-ttu-id="026cf-136">Der Wiederholungsversuch des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="026cf-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="026cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026cf-137">CommonParameters</span></span>
<span data-ttu-id="026cf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="026cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026cf-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="026cf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026cf-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="026cf-140">INPUTS</span></span>

### <span data-ttu-id="026cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="026cf-141">System.String</span></span>

### <span data-ttu-id="026cf-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="026cf-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="026cf-143">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="026cf-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="026cf-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="026cf-144">OUTPUTS</span></span>

### <span data-ttu-id="026cf-145">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="026cf-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="026cf-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="026cf-146">NOTES</span></span>

## <span data-ttu-id="026cf-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="026cf-147">RELATED LINKS</span></span>
