---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303454"
---
# <span data-ttu-id="dedfe-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="dedfe-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="dedfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dedfe-102">SYNOPSIS</span></span>
<span data-ttu-id="dedfe-103">Ruft die Verwendungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="dedfe-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="dedfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dedfe-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dedfe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dedfe-105">DESCRIPTION</span></span>
<span data-ttu-id="dedfe-106">Mit dem Cmdlet **Get-AzOperationalInsightsWorkspaceUsage werden** die Nutzungsdaten für einen Arbeitsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dedfe-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="dedfe-107">Dadurch wird festgestellt, wie viele Daten während eines bestimmten Zeitraums vom Arbeitsbereich analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="dedfe-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="dedfe-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dedfe-108">EXAMPLES</span></span>

### <span data-ttu-id="dedfe-109">Beispiel 1: Abrufen von Nutzungsdaten nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="dedfe-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="dedfe-110">Dieser Befehl ruft die Verwendungsdetails für den Arbeitsbereich mit dem Namen "myworkspace" in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="dedfe-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="dedfe-111">Beispiel 2: Abrufen von Verwendungsdaten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="dedfe-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="dedfe-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen "myworkspace" mithilfe des Get-AzOperationalInsightsWorkspace-Cmdlets ab und übergibt dann den Arbeitsbereich an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dedfe-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="dedfe-113">Der Befehl ruft die Nutzungsdetails für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="dedfe-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="dedfe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dedfe-114">PARAMETERS</span></span>

### <span data-ttu-id="dedfe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedfe-115">-DefaultProfile</span></span>
<span data-ttu-id="dedfe-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dedfe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dedfe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dedfe-117">-Name</span></span>
<span data-ttu-id="dedfe-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="dedfe-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="dedfe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedfe-119">-ResourceGroupName</span></span>
<span data-ttu-id="dedfe-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dedfe-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="dedfe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedfe-121">CommonParameters</span></span>
<span data-ttu-id="dedfe-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dedfe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedfe-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedfe-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedfe-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dedfe-124">INPUTS</span></span>

### <span data-ttu-id="dedfe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dedfe-125">System.String</span></span>

## <span data-ttu-id="dedfe-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dedfe-126">OUTPUTS</span></span>

### <span data-ttu-id="dedfe-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="dedfe-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="dedfe-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="dedfe-128">NOTES</span></span>

## <span data-ttu-id="dedfe-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dedfe-129">RELATED LINKS</span></span>

[<span data-ttu-id="dedfe-130">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="dedfe-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="dedfe-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="dedfe-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


