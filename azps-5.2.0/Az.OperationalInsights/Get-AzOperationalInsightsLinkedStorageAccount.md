---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301659"
---
# <span data-ttu-id="74e96-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74e96-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="74e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74e96-102">SYNOPSIS</span></span>
<span data-ttu-id="74e96-103">Verknüpftes Speicherkonto erhalten oder auflisten</span><span class="sxs-lookup"><span data-stu-id="74e96-103">Get or list linked storage account</span></span>

## <span data-ttu-id="74e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74e96-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74e96-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74e96-105">DESCRIPTION</span></span>
<span data-ttu-id="74e96-106">Verknüpftes Speicherkonto erhalten, alle verknüpften Speicherkonten auflisten, wenn "-DataSourceType" nicht angegeben wurde</span><span class="sxs-lookup"><span data-stu-id="74e96-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="74e96-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74e96-107">EXAMPLES</span></span>

### <span data-ttu-id="74e96-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74e96-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="74e96-109">Verknüpfte Speicheraufbewahrungen für Arbeitsbereich {workspace-name} auflisten</span><span class="sxs-lookup"><span data-stu-id="74e96-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="74e96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74e96-110">PARAMETERS</span></span>

### <span data-ttu-id="74e96-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="74e96-111">-DataSourceType</span></span>
<span data-ttu-id="74e96-112">Der Datenquellentyp sollte einer von "CustomLogs", "AzureTyp" sein.</span><span class="sxs-lookup"><span data-stu-id="74e96-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="74e96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e96-113">-DefaultProfile</span></span>
<span data-ttu-id="74e96-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74e96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74e96-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e96-115">-ResourceGroupName</span></span>
<span data-ttu-id="74e96-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74e96-116">The resource group name.</span></span>

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

### <span data-ttu-id="74e96-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74e96-117">-WorkspaceName</span></span>
<span data-ttu-id="74e96-118">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="74e96-118">The workspace name.</span></span>

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

### <span data-ttu-id="74e96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e96-119">CommonParameters</span></span>
<span data-ttu-id="74e96-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e96-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74e96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e96-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74e96-122">INPUTS</span></span>

### <span data-ttu-id="74e96-123">System.String</span><span class="sxs-lookup"><span data-stu-id="74e96-123">System.String</span></span>

## <span data-ttu-id="74e96-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74e96-124">OUTPUTS</span></span>

### <span data-ttu-id="74e96-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="74e96-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="74e96-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74e96-126">NOTES</span></span>

## <span data-ttu-id="74e96-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74e96-127">RELATED LINKS</span></span>