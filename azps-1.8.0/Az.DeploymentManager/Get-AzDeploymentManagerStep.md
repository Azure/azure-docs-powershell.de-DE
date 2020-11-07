---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661209"
---
# <span data-ttu-id="819f2-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="819f2-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="819f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="819f2-102">SYNOPSIS</span></span>
<span data-ttu-id="819f2-103">Ruft den Schritt ab.</span><span class="sxs-lookup"><span data-stu-id="819f2-103">Gets the step.</span></span>

## <span data-ttu-id="819f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="819f2-104">SYNTAX</span></span>

### <span data-ttu-id="819f2-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="819f2-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="819f2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="819f2-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="819f2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="819f2-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="819f2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="819f2-108">DESCRIPTION</span></span>
<span data-ttu-id="819f2-109">Das Cmdlet " **Get-AzDeploymentManagerStep** " Ruft einen Schritt ab und gibt ein Objekt zurück, das diesen Schritt darstellt.</span><span class="sxs-lookup"><span data-stu-id="819f2-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="819f2-110">Geben Sie den Schritt mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="819f2-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="819f2-111">Alternativ können Sie das Step-Objekt oder die "Resourcen-Nr" angeben.</span><span class="sxs-lookup"><span data-stu-id="819f2-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="819f2-112">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerStep-Cmdlets Änderungen an der Artefakt-Quelle übernehmen.</span><span class="sxs-lookup"><span data-stu-id="819f2-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="819f2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="819f2-113">EXAMPLES</span></span>

### <span data-ttu-id="819f2-114">Beispiel 1: Abrufen eines Schritts</span><span class="sxs-lookup"><span data-stu-id="819f2-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="819f2-115">Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="819f2-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="819f2-116">Beispiel 2: Abrufen eines Schritts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="819f2-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="819f2-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="819f2-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="819f2-118">Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="819f2-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="819f2-119">Beispiel 3: Abrufen eines Schritts mit einem von New-AzDeploymentManagerStep zurückgegebenen Objekt</span><span class="sxs-lookup"><span data-stu-id="819f2-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="819f2-120">Dieser Befehl ruft einen Schritt ab, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="819f2-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="819f2-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="819f2-121">PARAMETERS</span></span>

### <span data-ttu-id="819f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819f2-122">-DefaultProfile</span></span>
<span data-ttu-id="819f2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="819f2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="819f2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="819f2-124">-InputObject</span></span>
<span data-ttu-id="819f2-125">Das Step-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="819f2-125">The step resource object.</span></span>

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

### <span data-ttu-id="819f2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="819f2-126">-Name</span></span>
<span data-ttu-id="819f2-127">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="819f2-127">The name of the step.</span></span>

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

### <span data-ttu-id="819f2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819f2-128">-ResourceGroupName</span></span>
<span data-ttu-id="819f2-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="819f2-129">The resource group.</span></span>

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

### <span data-ttu-id="819f2-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="819f2-130">-ResourceId</span></span>
<span data-ttu-id="819f2-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="819f2-131">The resource identifier.</span></span>

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

### <span data-ttu-id="819f2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819f2-132">CommonParameters</span></span>
<span data-ttu-id="819f2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819f2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819f2-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819f2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819f2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="819f2-135">INPUTS</span></span>

### <span data-ttu-id="819f2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="819f2-136">System.String</span></span>

### <span data-ttu-id="819f2-137">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="819f2-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="819f2-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="819f2-138">OUTPUTS</span></span>

### <span data-ttu-id="819f2-139">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="819f2-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="819f2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="819f2-140">NOTES</span></span>

## <span data-ttu-id="819f2-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="819f2-141">RELATED LINKS</span></span>
