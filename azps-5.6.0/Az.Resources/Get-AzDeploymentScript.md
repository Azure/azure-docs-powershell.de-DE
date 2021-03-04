---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 7b61444bb4f3a23e1611e90b79545e1c174b0437
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920936"
---
# <span data-ttu-id="19545-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="19545-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="19545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19545-102">SYNOPSIS</span></span>
<span data-ttu-id="19545-103">Ruft Bereitstellungsskripts ab oder listet sie auf.</span><span class="sxs-lookup"><span data-stu-id="19545-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="19545-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19545-104">SYNTAX</span></span>

### <span data-ttu-id="19545-105">ListDeploymentScript (Standard)</span><span class="sxs-lookup"><span data-stu-id="19545-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19545-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="19545-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19545-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="19545-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19545-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19545-108">DESCRIPTION</span></span>
<span data-ttu-id="19545-109">Das **Get-AzDeploymentScript-Cmdlet** ruft ein einzelnes Bereitstellungsskript oder eine Liste der Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="19545-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="19545-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19545-110">EXAMPLES</span></span>

### <span data-ttu-id="19545-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19545-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="19545-112">Listet Bereitstellungsskripts im Abonnement im Kontext des aktuellen Benutzers auf.</span><span class="sxs-lookup"><span data-stu-id="19545-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="19545-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="19545-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="19545-114">Listet Bereitstellungsskripts in der Ressourcengruppe DS-TestRg auf.</span><span class="sxs-lookup"><span data-stu-id="19545-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="19545-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="19545-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="19545-116">Ruft ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG ab.</span><span class="sxs-lookup"><span data-stu-id="19545-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="19545-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="19545-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="19545-118">Ruft ein Bereitstellungsskript mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="19545-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="19545-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="19545-119">PARAMETERS</span></span>

### <span data-ttu-id="19545-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19545-120">-DefaultProfile</span></span>
<span data-ttu-id="19545-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19545-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19545-122">-ID</span><span class="sxs-lookup"><span data-stu-id="19545-122">-Id</span></span>
<span data-ttu-id="19545-123">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="19545-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="19545-124">Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="19545-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19545-125">-Name</span><span class="sxs-lookup"><span data-stu-id="19545-125">-Name</span></span>
<span data-ttu-id="19545-126">Der Name des Bereitstellungsskripts</span><span class="sxs-lookup"><span data-stu-id="19545-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19545-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19545-127">-ResourceGroupName</span></span>
<span data-ttu-id="19545-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="19545-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19545-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19545-129">CommonParameters</span></span>
<span data-ttu-id="19545-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19545-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="19545-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19545-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19545-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19545-132">INPUTS</span></span>

### <span data-ttu-id="19545-133">System.String</span><span class="sxs-lookup"><span data-stu-id="19545-133">System.String</span></span>

## <span data-ttu-id="19545-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19545-134">OUTPUTS</span></span>

### <span data-ttu-id="19545-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="19545-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="19545-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="19545-136">NOTES</span></span>

## <span data-ttu-id="19545-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="19545-137">RELATED LINKS</span></span>