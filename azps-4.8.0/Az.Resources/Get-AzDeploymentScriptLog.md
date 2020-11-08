---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174435"
---
# <span data-ttu-id="5e47d-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="5e47d-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="5e47d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e47d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e47d-103">Ruft das Protokoll einer Bereitstellung-Skriptausführung ab.</span><span class="sxs-lookup"><span data-stu-id="5e47d-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="5e47d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e47d-104">SYNTAX</span></span>

### <span data-ttu-id="5e47d-105">GetDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e47d-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e47d-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e47d-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e47d-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e47d-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e47d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e47d-108">DESCRIPTION</span></span>
<span data-ttu-id="5e47d-109">Das Cmdlet " **Get-AzDeploymentScriptLog** " Ruft das Protokoll einer Bereitstellungsskript Ausführung ab.</span><span class="sxs-lookup"><span data-stu-id="5e47d-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="5e47d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e47d-110">EXAMPLES</span></span>

### <span data-ttu-id="5e47d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e47d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="5e47d-112">Ruft das Protokoll eines Bereitstellungsskripts mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="5e47d-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="5e47d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5e47d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="5e47d-114">Ruft die letzten 3 Zeilen des Protokolls eines Bereitstellungsskripts mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="5e47d-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="5e47d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5e47d-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="5e47d-116">Der erste Befehl ruft ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="5e47d-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="5e47d-117">Der zweite Befehl ruft das Protokoll des angegebenen Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="5e47d-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="5e47d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e47d-118">PARAMETERS</span></span>

### <span data-ttu-id="5e47d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e47d-119">-DefaultProfile</span></span>
<span data-ttu-id="5e47d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e47d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e47d-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="5e47d-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="5e47d-122">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="5e47d-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="5e47d-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="5e47d-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="5e47d-124">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="5e47d-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="5e47d-125">Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="5e47d-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="5e47d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5e47d-126">-Name</span></span>
<span data-ttu-id="5e47d-127">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="5e47d-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="5e47d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e47d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e47d-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e47d-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e47d-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="5e47d-130">-Tail</span></span>
<span data-ttu-id="5e47d-131">Ausgabe auf letzte n Zeilen begrenzen</span><span class="sxs-lookup"><span data-stu-id="5e47d-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="5e47d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e47d-132">CommonParameters</span></span>
<span data-ttu-id="5e47d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e47d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e47d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e47d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e47d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e47d-135">INPUTS</span></span>

### <span data-ttu-id="5e47d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5e47d-136">System.String</span></span>

### <span data-ttu-id="5e47d-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="5e47d-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="5e47d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e47d-138">OUTPUTS</span></span>

### <span data-ttu-id="5e47d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="5e47d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="5e47d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e47d-140">NOTES</span></span>

## <span data-ttu-id="5e47d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e47d-141">RELATED LINKS</span></span>
