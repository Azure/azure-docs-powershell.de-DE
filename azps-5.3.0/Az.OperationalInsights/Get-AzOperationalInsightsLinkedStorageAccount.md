---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473322"
---
# <span data-ttu-id="5ee1f-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee1f-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5ee1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ee1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee1f-103">Verknüpftes Speicherkonto erhalten oder auflisten</span><span class="sxs-lookup"><span data-stu-id="5ee1f-103">Get or list linked storage account</span></span>

## <span data-ttu-id="5ee1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ee1f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee1f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ee1f-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee1f-106">Verknüpftes Speicherkonto erhalten, alle verknüpften Speicherkonten auflisten, wenn "-DataSourceType" nicht angegeben wurde</span><span class="sxs-lookup"><span data-stu-id="5ee1f-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="5ee1f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ee1f-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee1f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ee1f-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="5ee1f-109">Verknüpfte Speicheraufbewahrungen für Arbeitsbereich {workspace-name} auflisten</span><span class="sxs-lookup"><span data-stu-id="5ee1f-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="5ee1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ee1f-110">PARAMETERS</span></span>

### <span data-ttu-id="5ee1f-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="5ee1f-111">-DataSourceType</span></span>
<span data-ttu-id="5ee1f-112">Der Datenquellentyp sollte einer von "CustomLogs", "AzureDatson" sein.</span><span class="sxs-lookup"><span data-stu-id="5ee1f-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee1f-113">-DefaultProfile</span></span>
<span data-ttu-id="5ee1f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ee1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ee1f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee1f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ee1f-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ee1f-116">The resource group name.</span></span>

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

### <span data-ttu-id="5ee1f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ee1f-117">-WorkspaceName</span></span>
<span data-ttu-id="5ee1f-118">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5ee1f-118">The workspace name.</span></span>

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

### <span data-ttu-id="5ee1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee1f-119">CommonParameters</span></span>
<span data-ttu-id="5ee1f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee1f-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ee1f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee1f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ee1f-122">INPUTS</span></span>

### <span data-ttu-id="5ee1f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5ee1f-123">System.String</span></span>

## <span data-ttu-id="5ee1f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ee1f-124">OUTPUTS</span></span>

### <span data-ttu-id="5ee1f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="5ee1f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="5ee1f-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ee1f-126">NOTES</span></span>

## <span data-ttu-id="5ee1f-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ee1f-127">RELATED LINKS</span></span>