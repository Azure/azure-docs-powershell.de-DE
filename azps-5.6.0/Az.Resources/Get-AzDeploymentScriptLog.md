---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: dc62e4766a83e1a2046b15fbdf6619e08c4b8e28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920931"
---
# <span data-ttu-id="574ee-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="574ee-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="574ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="574ee-102">SYNOPSIS</span></span>
<span data-ttu-id="574ee-103">Ruft das Protokoll einer Ausführung eines Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="574ee-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="574ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="574ee-104">SYNTAX</span></span>

### <span data-ttu-id="574ee-105">GetDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="574ee-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="574ee-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="574ee-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="574ee-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="574ee-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="574ee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="574ee-108">DESCRIPTION</span></span>
<span data-ttu-id="574ee-109">Das **Get-AzDeploymentScriptLog-Cmdlet** ruft das Protokoll einer Ausführung eines Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="574ee-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="574ee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="574ee-110">EXAMPLES</span></span>

### <span data-ttu-id="574ee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="574ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="574ee-112">Ruft das Protokoll eines Bereitstellungsskripts mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG ab.</span><span class="sxs-lookup"><span data-stu-id="574ee-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="574ee-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="574ee-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="574ee-114">Ruft die letzten drei Zeilen des Protokolls eines Bereitstellungsskripts mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG ab.</span><span class="sxs-lookup"><span data-stu-id="574ee-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="574ee-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="574ee-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="574ee-116">Der erste Befehl ruft ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG ab.</span><span class="sxs-lookup"><span data-stu-id="574ee-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="574ee-117">Der zweite Befehl ruft das Protokoll eines bestimmten Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="574ee-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="574ee-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="574ee-118">PARAMETERS</span></span>

### <span data-ttu-id="574ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574ee-119">-DefaultProfile</span></span>
<span data-ttu-id="574ee-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="574ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="574ee-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="574ee-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="574ee-122">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="574ee-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="574ee-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="574ee-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="574ee-124">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="574ee-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="574ee-125">Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="574ee-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574ee-126">-Name</span><span class="sxs-lookup"><span data-stu-id="574ee-126">-Name</span></span>
<span data-ttu-id="574ee-127">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="574ee-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574ee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574ee-128">-ResourceGroupName</span></span>
<span data-ttu-id="574ee-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="574ee-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574ee-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="574ee-130">-Tail</span></span>
<span data-ttu-id="574ee-131">Ausgabe auf letzte n Zeilen beschränken</span><span class="sxs-lookup"><span data-stu-id="574ee-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574ee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574ee-132">CommonParameters</span></span>
<span data-ttu-id="574ee-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="574ee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574ee-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="574ee-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574ee-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="574ee-135">INPUTS</span></span>

### <span data-ttu-id="574ee-136">System.String</span><span class="sxs-lookup"><span data-stu-id="574ee-136">System.String</span></span>

### <span data-ttu-id="574ee-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="574ee-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="574ee-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="574ee-138">OUTPUTS</span></span>

### <span data-ttu-id="574ee-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="574ee-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="574ee-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="574ee-140">NOTES</span></span>

## <span data-ttu-id="574ee-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="574ee-141">RELATED LINKS</span></span>
