---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004525"
---
# <span data-ttu-id="e2b85-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="e2b85-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="e2b85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2b85-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b85-103">Ruft das Protokoll einer Bereitstellung-Skriptausführung ab.</span><span class="sxs-lookup"><span data-stu-id="e2b85-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="e2b85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2b85-104">SYNTAX</span></span>

### <span data-ttu-id="e2b85-105">GetDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2b85-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b85-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2b85-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b85-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2b85-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2b85-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2b85-108">DESCRIPTION</span></span>
<span data-ttu-id="e2b85-109">Das Cmdlet " **Get-AzDeploymentScriptLog** " Ruft das Protokoll einer Bereitstellungsskript Ausführung ab.</span><span class="sxs-lookup"><span data-stu-id="e2b85-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="e2b85-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2b85-110">EXAMPLES</span></span>

### <span data-ttu-id="e2b85-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2b85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="e2b85-112">Ruft das Protokoll eines Bereitstellungsskripts mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="e2b85-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="e2b85-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2b85-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="e2b85-114">Der erste Befehl ruft ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="e2b85-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="e2b85-115">Der zweite Befehl ruft das Protokoll des angegebenen Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="e2b85-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="e2b85-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2b85-116">PARAMETERS</span></span>

### <span data-ttu-id="e2b85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b85-117">-DefaultProfile</span></span>
<span data-ttu-id="e2b85-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2b85-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b85-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="e2b85-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="e2b85-120">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="e2b85-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b85-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="e2b85-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="e2b85-122">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="e2b85-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="e2b85-123">Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="e2b85-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b85-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e2b85-124">-Name</span></span>
<span data-ttu-id="e2b85-125">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="e2b85-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b85-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2b85-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e2b85-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b85-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b85-128">CommonParameters</span></span>
<span data-ttu-id="e2b85-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b85-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e2b85-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b85-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b85-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2b85-131">INPUTS</span></span>

### <span data-ttu-id="e2b85-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e2b85-132">System.String</span></span>

### <span data-ttu-id="e2b85-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="e2b85-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="e2b85-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2b85-134">OUTPUTS</span></span>

### <span data-ttu-id="e2b85-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="e2b85-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="e2b85-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2b85-136">NOTES</span></span>

## <span data-ttu-id="e2b85-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2b85-137">RELATED LINKS</span></span>
