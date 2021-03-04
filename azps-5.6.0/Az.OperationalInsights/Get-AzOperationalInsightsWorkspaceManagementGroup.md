---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 505156f1c6303b8a3fa699b5528ed3ca2ff690de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938523"
---
# <span data-ttu-id="f8919-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8919-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="f8919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8919-102">SYNOPSIS</span></span>
<span data-ttu-id="f8919-103">Ruft Details zu Verwaltungsgruppen ab, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="f8919-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="f8919-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8919-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8919-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8919-105">DESCRIPTION</span></span>
<span data-ttu-id="f8919-106">Im **Cmdlet Get-AzOperationalInsightsWorkspaceManagementGroup** werden die Verwaltungsgruppen aufgeführt, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="f8919-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="f8919-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8919-107">EXAMPLES</span></span>

### <span data-ttu-id="f8919-108">Beispiel 1: Erhalten von Verwaltungsgruppen nach Arbeitsbereichsname</span><span class="sxs-lookup"><span data-stu-id="f8919-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="f8919-109">Dieser Befehl ruft die Verwaltungsgruppen für den Arbeitsbereich mit dem Namen MyWorkspace in der Ressourcengruppe namens ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="f8919-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f8919-110">Beispiel 2: Erhalten von Verwaltungsgruppen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8919-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="f8919-111">Dieser Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkspace zu erhalten, und übergibt den Arbeitsbereich dann an das aktuelle Cmdlet, das die Verwaltungsgruppen für diesen Arbeitsbereich erhält.</span><span class="sxs-lookup"><span data-stu-id="f8919-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="f8919-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f8919-112">PARAMETERS</span></span>

### <span data-ttu-id="f8919-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8919-113">-DefaultProfile</span></span>
<span data-ttu-id="f8919-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f8919-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8919-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f8919-115">-Name</span></span>
<span data-ttu-id="f8919-116">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="f8919-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f8919-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8919-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8919-118">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f8919-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="f8919-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8919-119">CommonParameters</span></span>
<span data-ttu-id="f8919-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8919-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8919-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8919-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8919-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8919-122">INPUTS</span></span>

### <span data-ttu-id="f8919-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f8919-123">System.String</span></span>

## <span data-ttu-id="f8919-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8919-124">OUTPUTS</span></span>

### <span data-ttu-id="f8919-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8919-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="f8919-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f8919-126">NOTES</span></span>

## <span data-ttu-id="f8919-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f8919-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8919-128">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f8919-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="f8919-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f8919-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


