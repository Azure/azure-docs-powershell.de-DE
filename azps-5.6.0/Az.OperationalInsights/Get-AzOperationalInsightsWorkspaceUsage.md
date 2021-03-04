---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: b5b14cbf816a7872abf431f787f9e3102006901c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944818"
---
# <span data-ttu-id="0b107-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="0b107-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="0b107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b107-102">SYNOPSIS</span></span>
<span data-ttu-id="0b107-103">Ruft die Nutzungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0b107-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="0b107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b107-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b107-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b107-105">DESCRIPTION</span></span>
<span data-ttu-id="0b107-106">Das **Get-AzOperationalInsightsWorkspaceUsage-Cmdlet** ruft die Nutzungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0b107-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="0b107-107">Dadurch wird angezeigt, wie viele Daten vom Arbeitsbereich über einen bestimmten Zeitraum analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0b107-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="0b107-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b107-108">EXAMPLES</span></span>

### <span data-ttu-id="0b107-109">Beispiel 1: Verwenden von Daten nach Arbeitsbereichsname</span><span class="sxs-lookup"><span data-stu-id="0b107-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0b107-110">Dieser Befehl ruft die Verwendungsdetails für den Arbeitsbereich mit dem Namen MyWorkspace in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0b107-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="0b107-111">Beispiel 2: Verwenden der Pipeline zum Verwenden von Nutzungsdaten</span><span class="sxs-lookup"><span data-stu-id="0b107-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="0b107-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen MyWorkSpace mit dem cmdlet Get-AzOperationalInsightsWorkspace ab und übergibt den Arbeitsbereich dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b107-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="0b107-113">Der Befehl ruft die Nutzungsdetails für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0b107-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="0b107-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b107-114">PARAMETERS</span></span>

### <span data-ttu-id="0b107-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b107-115">-DefaultProfile</span></span>
<span data-ttu-id="0b107-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0b107-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b107-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0b107-117">-Name</span></span>
<span data-ttu-id="0b107-118">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="0b107-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0b107-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b107-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b107-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b107-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0b107-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b107-121">CommonParameters</span></span>
<span data-ttu-id="0b107-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b107-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b107-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b107-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b107-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b107-124">INPUTS</span></span>

### <span data-ttu-id="0b107-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0b107-125">System.String</span></span>

## <span data-ttu-id="0b107-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b107-126">OUTPUTS</span></span>

### <span data-ttu-id="0b107-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="0b107-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="0b107-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b107-128">NOTES</span></span>

## <span data-ttu-id="0b107-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b107-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b107-130">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b107-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="0b107-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b107-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


