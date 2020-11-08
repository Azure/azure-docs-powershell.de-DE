---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173168"
---
# <span data-ttu-id="7134b-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="7134b-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="7134b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7134b-102">SYNOPSIS</span></span>
<span data-ttu-id="7134b-103">Abrufen oder Auflisten eines verknüpften Diensts für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7134b-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="7134b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7134b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7134b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7134b-105">DESCRIPTION</span></span>
<span data-ttu-id="7134b-106">Abrufen oder Auflisten des verknüpften Diensts für Workspace, Liste, wenn "-LinkedServiceName" nicht bereitgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="7134b-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="7134b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7134b-107">EXAMPLES</span></span>

### <span data-ttu-id="7134b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7134b-108">Example 1</span></span>
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

<span data-ttu-id="7134b-109">Abrufen des verknüpften Diensts für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7134b-109">Get linked service for workspace</span></span>

## <span data-ttu-id="7134b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7134b-110">PARAMETERS</span></span>

### <span data-ttu-id="7134b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7134b-111">-DefaultProfile</span></span>
<span data-ttu-id="7134b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7134b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7134b-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="7134b-113">-LinkedServiceName</span></span>
<span data-ttu-id="7134b-114">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="7134b-114">The linked service name.</span></span>

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

### <span data-ttu-id="7134b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7134b-115">-ResourceGroupName</span></span>
<span data-ttu-id="7134b-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7134b-116">The resource group name.</span></span>

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

### <span data-ttu-id="7134b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7134b-117">-WorkspaceName</span></span>
<span data-ttu-id="7134b-118">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="7134b-118">The workspace name.</span></span>

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

### <span data-ttu-id="7134b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7134b-119">CommonParameters</span></span>
<span data-ttu-id="7134b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7134b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7134b-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7134b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7134b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7134b-122">INPUTS</span></span>

### <span data-ttu-id="7134b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7134b-123">System.String</span></span>

## <span data-ttu-id="7134b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7134b-124">OUTPUTS</span></span>

### <span data-ttu-id="7134b-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="7134b-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="7134b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7134b-126">NOTES</span></span>

## <span data-ttu-id="7134b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7134b-127">RELATED LINKS</span></span>
