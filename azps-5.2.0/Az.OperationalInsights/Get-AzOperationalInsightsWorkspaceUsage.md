---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360742"
---
# <span data-ttu-id="19db4-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="19db4-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="19db4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19db4-102">SYNOPSIS</span></span>
<span data-ttu-id="19db4-103">Ruft die Nutzungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="19db4-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="19db4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19db4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19db4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19db4-105">DESCRIPTION</span></span>
<span data-ttu-id="19db4-106">Das **Cmdlet "Get-AzOperationalInsightsWorkspaceUsage"** ruft die Nutzungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="19db4-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="19db4-107">Dadurch wird angezeigt, wie viele Daten über einen bestimmten Zeitraum vom Arbeitsbereich analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="19db4-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="19db4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19db4-108">EXAMPLES</span></span>

### <span data-ttu-id="19db4-109">Beispiel 1: Nutzungsdaten nach Arbeitsbereichsname erhalten</span><span class="sxs-lookup"><span data-stu-id="19db4-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="19db4-110">Dieser Befehl ruft die Verwendungsdetails für den Arbeitsbereich mit dem Namen "MeinWorkspace" in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="19db4-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="19db4-111">Beispiel 2: Erhalten von Nutzungsdaten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="19db4-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="19db4-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen "MyWorkSpace" mithilfe des cmdlets Get-AzOperationalInsightsWorkspace ab und übergibt den Arbeitsbereich dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19db4-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="19db4-113">Der Befehl ruft die Nutzungsdetails für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="19db4-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="19db4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19db4-114">PARAMETERS</span></span>

### <span data-ttu-id="19db4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19db4-115">-DefaultProfile</span></span>
<span data-ttu-id="19db4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="19db4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19db4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="19db4-117">-Name</span></span>
<span data-ttu-id="19db4-118">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="19db4-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="19db4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19db4-119">-ResourceGroupName</span></span>
<span data-ttu-id="19db4-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="19db4-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="19db4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19db4-121">CommonParameters</span></span>
<span data-ttu-id="19db4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19db4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19db4-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19db4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19db4-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19db4-124">INPUTS</span></span>

### <span data-ttu-id="19db4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="19db4-125">System.String</span></span>

## <span data-ttu-id="19db4-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19db4-126">OUTPUTS</span></span>

### <span data-ttu-id="19db4-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="19db4-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="19db4-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19db4-128">NOTES</span></span>

## <span data-ttu-id="19db4-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19db4-129">RELATED LINKS</span></span>

[<span data-ttu-id="19db4-130">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="19db4-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="19db4-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="19db4-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


