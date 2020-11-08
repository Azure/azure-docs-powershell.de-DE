---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: c1054e8dfb9a9133da740c5162c8e8f60c9df5d1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007481"
---
# <span data-ttu-id="a7cb3-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="a7cb3-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="a7cb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cb3-103">Ruft die Verwendungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="a7cb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7cb3-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7cb3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="a7cb3-106">Mit dem Cmdlet **Get-AzOperationalInsightsWorkspaceUsage werden** die Nutzungsdaten für einen Arbeitsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="a7cb3-107">Dadurch wird festgestellt, wie viele Daten während eines bestimmten Zeitraums vom Arbeitsbereich analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="a7cb3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7cb3-108">EXAMPLES</span></span>

### <span data-ttu-id="a7cb3-109">Beispiel 1: Abrufen von Nutzungsdaten nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="a7cb3-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="a7cb3-110">Dieser Befehl ruft die Verwendungsdetails für den Arbeitsbereich mit dem Namen "myworkspace" in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="a7cb3-111">Beispiel 2: Abrufen von Verwendungsdaten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a7cb3-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="a7cb3-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen "myworkspace" mithilfe des Get-AzOperationalInsightsWorkspace-Cmdlets ab und übergibt dann den Arbeitsbereich an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="a7cb3-113">Der Befehl ruft die Nutzungsdetails für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="a7cb3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7cb3-114">PARAMETERS</span></span>

### <span data-ttu-id="a7cb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cb3-115">-DefaultProfile</span></span>
<span data-ttu-id="a7cb3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a7cb3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7cb3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a7cb3-117">-Name</span></span>
<span data-ttu-id="a7cb3-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a7cb3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7cb3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7cb3-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="a7cb3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cb3-121">CommonParameters</span></span>
<span data-ttu-id="a7cb3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7cb3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cb3-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7cb3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cb3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7cb3-124">INPUTS</span></span>

### <span data-ttu-id="a7cb3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a7cb3-125">System.String</span></span>

## <span data-ttu-id="a7cb3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7cb3-126">OUTPUTS</span></span>

### <span data-ttu-id="a7cb3-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="a7cb3-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="a7cb3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7cb3-128">NOTES</span></span>

## <span data-ttu-id="a7cb3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7cb3-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7cb3-130">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a7cb3-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="a7cb3-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a7cb3-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


