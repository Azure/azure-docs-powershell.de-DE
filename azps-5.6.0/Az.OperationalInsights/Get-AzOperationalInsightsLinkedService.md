---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 71a715386a4d5646f1c9015244ad8a096313bb64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925416"
---
# <span data-ttu-id="57a6f-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="57a6f-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="57a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="57a6f-103">Zugreifen oder Auflisten von verknüpften Dienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="57a6f-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="57a6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57a6f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57a6f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="57a6f-106">Verknüpften Dienst für Arbeitsbereich anzeigen oder auflisten, Liste, wenn "-LinkedServiceName" nicht bereitgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="57a6f-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="57a6f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57a6f-107">EXAMPLES</span></span>

### <span data-ttu-id="57a6f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57a6f-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="57a6f-109">Verknüpften Dienst für Arbeitsbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="57a6f-109">Get linked service for workspace</span></span>

## <span data-ttu-id="57a6f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="57a6f-110">PARAMETERS</span></span>

### <span data-ttu-id="57a6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a6f-111">-DefaultProfile</span></span>
<span data-ttu-id="57a6f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57a6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a6f-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="57a6f-113">-LinkedServiceName</span></span>
<span data-ttu-id="57a6f-114">Der name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="57a6f-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="57a6f-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57a6f-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a6f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="57a6f-117">-WorkspaceName</span></span>
<span data-ttu-id="57a6f-118">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="57a6f-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a6f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a6f-119">CommonParameters</span></span>
<span data-ttu-id="57a6f-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a6f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a6f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57a6f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a6f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57a6f-122">INPUTS</span></span>

### <span data-ttu-id="57a6f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="57a6f-123">System.String</span></span>

## <span data-ttu-id="57a6f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57a6f-124">OUTPUTS</span></span>

### <span data-ttu-id="57a6f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="57a6f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="57a6f-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="57a6f-126">NOTES</span></span>

## <span data-ttu-id="57a6f-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="57a6f-127">RELATED LINKS</span></span>
