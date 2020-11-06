---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474834"
---
# <span data-ttu-id="c7cf2-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c7cf2-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="c7cf2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cf2-103">Ruft den Bereitstellungsschritt ab.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-103">Gets the deployment step.</span></span>

## <span data-ttu-id="c7cf2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7cf2-104">SYNTAX</span></span>

### <span data-ttu-id="c7cf2-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7cf2-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7cf2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7cf2-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7cf2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7cf2-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7cf2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7cf2-108">DESCRIPTION</span></span>
<span data-ttu-id="c7cf2-109">Das Cmdlet " **Get-AzureRmDeploymentManagerStep** " Ruft einen Schritt ab und gibt ein Objekt zurück, das diesen Schritt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="c7cf2-110">Geben Sie den Schritt mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="c7cf2-111">Alternativ können Sie das Step-Objekt oder die "Resourcen-Nr" angeben.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="c7cf2-112">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerStep-Cmdlets Änderungen an der Artefakt-Quelle übernehmen.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="c7cf2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7cf2-113">EXAMPLES</span></span>

### <span data-ttu-id="c7cf2-114">Beispiel 1: Abrufen eines Schritts</span><span class="sxs-lookup"><span data-stu-id="c7cf2-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="c7cf2-115">Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c7cf2-116">Beispiel 2: Abrufen eines Schritts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="c7cf2-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="c7cf2-117">Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c7cf2-118">Beispiel 3: Abrufen eines Schritts mit einem von New-AzureRmDeploymentManagerStep zurückgegebenen Objekt</span><span class="sxs-lookup"><span data-stu-id="c7cf2-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="c7cf2-119">Dieser Befehl ruft einen Schritt ab, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="c7cf2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7cf2-120">PARAMETERS</span></span>

### <span data-ttu-id="c7cf2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cf2-121">-DefaultProfile</span></span>
<span data-ttu-id="c7cf2-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7cf2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c7cf2-123">-Name</span></span>
<span data-ttu-id="c7cf2-124">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-124">The name of the step.</span></span>

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

### <span data-ttu-id="c7cf2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7cf2-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7cf2-126">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-126">The resource group.</span></span>

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

### <span data-ttu-id="c7cf2-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c7cf2-127">-ResourceId</span></span>
<span data-ttu-id="c7cf2-128">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-128">The resource identifier.</span></span>

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

### <span data-ttu-id="c7cf2-129">-Step</span><span class="sxs-lookup"><span data-stu-id="c7cf2-129">-Step</span></span>
<span data-ttu-id="c7cf2-130">Das Step-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-130">The step resource object.</span></span>

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

### <span data-ttu-id="c7cf2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cf2-131">CommonParameters</span></span>
<span data-ttu-id="c7cf2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7cf2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c7cf2-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7cf2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cf2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7cf2-134">INPUTS</span></span>

### <span data-ttu-id="c7cf2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c7cf2-135">System.String</span></span>

### <span data-ttu-id="c7cf2-136">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c7cf2-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c7cf2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7cf2-137">OUTPUTS</span></span>

### <span data-ttu-id="c7cf2-138">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c7cf2-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c7cf2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7cf2-139">NOTES</span></span>

## <span data-ttu-id="c7cf2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7cf2-140">RELATED LINKS</span></span>
