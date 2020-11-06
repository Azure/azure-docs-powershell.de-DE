---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474581"
---
# <span data-ttu-id="c4e4b-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e4b-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="c4e4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e4b-103">Ruft ein Rollout ab.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-103">Gets a rollout.</span></span>

## <span data-ttu-id="c4e4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4e4b-104">SYNTAX</span></span>

### <span data-ttu-id="c4e4b-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4e4b-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e4b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e4b-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4e4b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e4b-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4e4b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4e4b-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e4b-109">Das Cmdlet " **Get-AzureRmDeploymentManagerRollout** " Ruft ein Rollout ab und gibt ein Objekt zurück, das diesen Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="c4e4b-110">Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="c4e4b-111">Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="c4e4b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4e4b-112">EXAMPLES</span></span>

### <span data-ttu-id="c4e4b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4e4b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="c4e4b-114">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c4e4b-115">Beispiel 2: Abrufen eines Rollouts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="c4e4b-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="c4e4b-116">Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c4e4b-117">Beispiel 3: Abrufen eines Rollouts mithilfe des Rollout-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="c4e4b-118">Dieser Befehl ruft ein Rollout ab, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="c4e4b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4e4b-119">PARAMETERS</span></span>

### <span data-ttu-id="c4e4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e4b-120">-DefaultProfile</span></span>
<span data-ttu-id="c4e4b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e4b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c4e4b-122">-Name</span></span>
<span data-ttu-id="c4e4b-123">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-123">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e4b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e4b-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4e4b-125">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e4b-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c4e4b-126">-ResourceId</span></span>
<span data-ttu-id="c4e4b-127">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-127">The resource identifier.</span></span>

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

### <span data-ttu-id="c4e4b-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="c4e4b-128">-RetryAttempt</span></span>
<span data-ttu-id="c4e4b-129">Der Wiederholungsversuch des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e4b-130">-Rollout</span><span class="sxs-lookup"><span data-stu-id="c4e4b-130">-Rollout</span></span>
<span data-ttu-id="c4e4b-131">Rollout-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-131">Rollout object.</span></span>

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

### <span data-ttu-id="c4e4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e4b-132">CommonParameters</span></span>
<span data-ttu-id="c4e4b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e4b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e4b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4e4b-135">INPUTS</span></span>

### <span data-ttu-id="c4e4b-136">Keine</span><span class="sxs-lookup"><span data-stu-id="c4e4b-136">None</span></span>

## <span data-ttu-id="c4e4b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4e4b-137">OUTPUTS</span></span>

### <span data-ttu-id="c4e4b-138">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="c4e4b-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c4e4b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4e4b-139">NOTES</span></span>

## <span data-ttu-id="c4e4b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4e4b-140">RELATED LINKS</span></span>

[<span data-ttu-id="c4e4b-141">Stopp-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e4b-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="c4e4b-142">Neustart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e4b-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="c4e4b-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c4e4b-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)