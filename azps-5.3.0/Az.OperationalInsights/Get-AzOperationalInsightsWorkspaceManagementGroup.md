---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473318"
---
# <span data-ttu-id="7250a-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7250a-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="7250a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7250a-102">SYNOPSIS</span></span>
<span data-ttu-id="7250a-103">Ruft Details zu Verwaltungsgruppen ab, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="7250a-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="7250a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7250a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7250a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7250a-105">DESCRIPTION</span></span>
<span data-ttu-id="7250a-106">Das **Cmdlet "Get-AzOperationalInsightsWorkspaceManagementGroup"** listet die Verwaltungsgruppen auf, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="7250a-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="7250a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7250a-107">EXAMPLES</span></span>

### <span data-ttu-id="7250a-108">Beispiel 1: Erhalten von Verwaltungsgruppen nach Dem Namen des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7250a-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="7250a-109">Mit diesem Befehl werden die Verwaltungsgruppen für den Arbeitsbereich namens "MyWorkspace" in der Ressourcengruppe "ContosoResourceGroup" ruft.</span><span class="sxs-lookup"><span data-stu-id="7250a-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="7250a-110">Beispiel 2: Erhalten von Verwaltungsgruppen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="7250a-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="7250a-111">Dieser Befehl verwendet das Cmdlet Get-AzOperationalInsightsWorkspace, um den Arbeitsbereich "MyWorkspace" zu erhalten, und übergibt den Arbeitsbereich dann an das aktuelle Cmdlet, das die Verwaltungsgruppen für diesen Arbeitsbereich erhält.</span><span class="sxs-lookup"><span data-stu-id="7250a-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="7250a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7250a-112">PARAMETERS</span></span>

### <span data-ttu-id="7250a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7250a-113">-DefaultProfile</span></span>
<span data-ttu-id="7250a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7250a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7250a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7250a-115">-Name</span></span>
<span data-ttu-id="7250a-116">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="7250a-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7250a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7250a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7250a-118">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7250a-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7250a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7250a-119">CommonParameters</span></span>
<span data-ttu-id="7250a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7250a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7250a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7250a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7250a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7250a-122">INPUTS</span></span>

### <span data-ttu-id="7250a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7250a-123">System.String</span></span>

## <span data-ttu-id="7250a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7250a-124">OUTPUTS</span></span>

### <span data-ttu-id="7250a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7250a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="7250a-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7250a-126">NOTES</span></span>

## <span data-ttu-id="7250a-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7250a-127">RELATED LINKS</span></span>

[<span data-ttu-id="7250a-128">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7250a-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="7250a-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7250a-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


