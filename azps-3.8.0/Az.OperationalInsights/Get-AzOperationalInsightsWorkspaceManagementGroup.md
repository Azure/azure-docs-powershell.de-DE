---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: c89938b677809fbdd8679411e0d6108d407afc6a
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007483"
---
# <span data-ttu-id="9f1e0-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9f1e0-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="9f1e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1e0-103">Ruft Details zu Verwaltungsgruppen ab, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="9f1e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f1e0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f1e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1e0-106">Das Cmdlet " **Get-AzOperationalInsightsWorkspaceManagementGroup** " listet die Verwaltungsgruppen auf, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="9f1e0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f1e0-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1e0-108">Beispiel 1: Abrufen von Verwaltungsgruppen nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="9f1e0-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="9f1e0-109">Dieser Befehl ruft die Verwaltungsgruppen für den Arbeitsbereich mit dem Namen myworkspace in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="9f1e0-110">Beispiel 2: Abrufen von Verwaltungsgruppen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="9f1e0-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="9f1e0-111">Dieser Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt dann den Arbeitsbereich an das aktuelle Cmdlet, das die Verwaltungsgruppen für diesen Arbeitsbereich abruft.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="9f1e0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f1e0-112">PARAMETERS</span></span>

### <span data-ttu-id="9f1e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1e0-113">-DefaultProfile</span></span>
<span data-ttu-id="9f1e0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f1e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f1e0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9f1e0-115">-Name</span></span>
<span data-ttu-id="9f1e0-116">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="9f1e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f1e0-118">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="9f1e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1e0-119">CommonParameters</span></span>
<span data-ttu-id="9f1e0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1e0-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f1e0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1e0-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f1e0-122">INPUTS</span></span>

### <span data-ttu-id="9f1e0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9f1e0-123">System.String</span></span>

## <span data-ttu-id="9f1e0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f1e0-124">OUTPUTS</span></span>

### <span data-ttu-id="9f1e0-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9f1e0-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="9f1e0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f1e0-126">NOTES</span></span>

## <span data-ttu-id="9f1e0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f1e0-127">RELATED LINKS</span></span>

[<span data-ttu-id="9f1e0-128">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="9f1e0-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="9f1e0-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f1e0-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


