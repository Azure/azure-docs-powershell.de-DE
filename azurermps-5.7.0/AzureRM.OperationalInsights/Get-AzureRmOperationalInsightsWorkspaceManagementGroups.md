---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 808c92e987d30e97ee0ad2ed56b24be9b0f92a1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662460"
---
# <span data-ttu-id="76a08-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="76a08-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="76a08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76a08-102">SYNOPSIS</span></span>
<span data-ttu-id="76a08-103">Ruft Details zu Verwaltungsgruppen ab, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="76a08-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76a08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76a08-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a08-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76a08-105">DESCRIPTION</span></span>
<span data-ttu-id="76a08-106">Das Cmdlet " **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** " listet die Verwaltungsgruppen auf, die mit einem Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="76a08-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="76a08-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76a08-107">EXAMPLES</span></span>

### <span data-ttu-id="76a08-108">Beispiel 1: Abrufen von Verwaltungsgruppen nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="76a08-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="76a08-109">Dieser Befehl ruft die Verwaltungsgruppen für den Arbeitsbereich mit dem Namen myworkspace in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="76a08-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="76a08-110">Beispiel 2: Abrufen von Verwaltungsgruppen mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="76a08-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="76a08-111">Dieser Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt dann den Arbeitsbereich an das aktuelle Cmdlet, das die Verwaltungsgruppen für diesen Arbeitsbereich abruft.</span><span class="sxs-lookup"><span data-stu-id="76a08-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="76a08-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="76a08-112">PARAMETERS</span></span>

### <span data-ttu-id="76a08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a08-113">-DefaultProfile</span></span>
<span data-ttu-id="76a08-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="76a08-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a08-115">-Name</span><span class="sxs-lookup"><span data-stu-id="76a08-115">-Name</span></span>
<span data-ttu-id="76a08-116">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="76a08-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a08-117">-ResourceGroupName</span></span>
<span data-ttu-id="76a08-118">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="76a08-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a08-119">CommonParameters</span></span>
<span data-ttu-id="76a08-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a08-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a08-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a08-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76a08-122">INPUTS</span></span>

### <span data-ttu-id="76a08-123">Keine</span><span class="sxs-lookup"><span data-stu-id="76a08-123">None</span></span>
<span data-ttu-id="76a08-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="76a08-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76a08-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76a08-125">OUTPUTS</span></span>

### <span data-ttu-id="76a08-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="76a08-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="76a08-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="76a08-127">NOTES</span></span>

## <span data-ttu-id="76a08-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76a08-128">RELATED LINKS</span></span>

[<span data-ttu-id="76a08-129">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="76a08-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="76a08-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="76a08-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


