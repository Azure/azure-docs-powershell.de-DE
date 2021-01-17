---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459816"
---
# <span data-ttu-id="2043e-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="2043e-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="2043e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2043e-102">SYNOPSIS</span></span>
<span data-ttu-id="2043e-103">Ruft Informationen zu einem Speicherinblick ab.</span><span class="sxs-lookup"><span data-stu-id="2043e-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="2043e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2043e-104">SYNTAX</span></span>

### <span data-ttu-id="2043e-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2043e-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2043e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2043e-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2043e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2043e-107">DESCRIPTION</span></span>
<span data-ttu-id="2043e-108">Das **Cmdlet "Get-AzOperationalInsightsStorageInsight"** ruft Informationen über einen vorhandenen Speichereinblick ab.</span><span class="sxs-lookup"><span data-stu-id="2043e-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="2043e-109">Wenn ein Name für die Speichereinblicke angegeben wird, ruft dieses Cmdlet Informationen zu diesem Speichereinblick ab.</span><span class="sxs-lookup"><span data-stu-id="2043e-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="2043e-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Speichereinblicken in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2043e-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="2043e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2043e-111">EXAMPLES</span></span>

### <span data-ttu-id="2043e-112">Beispiel 1: Erhalten eines Speicherinblicks nach Name</span><span class="sxs-lookup"><span data-stu-id="2043e-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="2043e-113">Dieser Befehl ruft den Speichereinblick "MyStorageInsight" aus dem Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="2043e-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2043e-114">Beispiel 2: Erhalten eines Speicherblicks mithilfe eines Arbeitsbereichsobjekts</span><span class="sxs-lookup"><span data-stu-id="2043e-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="2043e-115">Der erste Befehl verwendet das **Cmdlet "Get-AzOperationalInsightsWorkspace",** um einen Arbeitsbereich für Operational Insights zu erhalten, und speichert ihn dann in der $Workspace Variable.</span><span class="sxs-lookup"><span data-stu-id="2043e-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="2043e-116">Der zweite Befehl ruft den Speichereinblick "MyStorageInsight" für den Arbeitsbereich in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="2043e-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="2043e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2043e-117">PARAMETERS</span></span>

### <span data-ttu-id="2043e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2043e-118">-DefaultProfile</span></span>
<span data-ttu-id="2043e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2043e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2043e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2043e-120">-Name</span></span>
<span data-ttu-id="2043e-121">Gibt den Namen der Speicherinblicke an.</span><span class="sxs-lookup"><span data-stu-id="2043e-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2043e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2043e-122">-ResourceGroupName</span></span>
<span data-ttu-id="2043e-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2043e-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2043e-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="2043e-124">-Workspace</span></span>
<span data-ttu-id="2043e-125">Gibt den Arbeitsbereich an, der die Speichereinblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="2043e-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2043e-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2043e-126">-WorkspaceName</span></span>
<span data-ttu-id="2043e-127">Gibt den Namen des Arbeitsbereichs an, der die Speichereinblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="2043e-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2043e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2043e-128">CommonParameters</span></span>
<span data-ttu-id="2043e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2043e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2043e-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2043e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2043e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2043e-131">INPUTS</span></span>

### <span data-ttu-id="2043e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2043e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2043e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2043e-133">System.String</span></span>

## <span data-ttu-id="2043e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2043e-134">OUTPUTS</span></span>

### <span data-ttu-id="2043e-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="2043e-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="2043e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2043e-136">NOTES</span></span>

## <span data-ttu-id="2043e-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2043e-137">RELATED LINKS</span></span>

[<span data-ttu-id="2043e-138">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2043e-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


