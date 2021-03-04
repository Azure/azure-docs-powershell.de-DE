---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930864"
---
# <span data-ttu-id="4715b-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4715b-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="4715b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4715b-102">SYNOPSIS</span></span>
<span data-ttu-id="4715b-103">Erstellen oder Auflisten eines verknüpften Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="4715b-103">Get or list linked storage account</span></span>

## <span data-ttu-id="4715b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4715b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4715b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4715b-105">DESCRIPTION</span></span>
<span data-ttu-id="4715b-106">Verknüpftes Speicherkonto erhalten, Alle verknüpften Speicherkonten auflisten, wenn "-DataSourceType" nicht angegeben wurde</span><span class="sxs-lookup"><span data-stu-id="4715b-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="4715b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4715b-107">EXAMPLES</span></span>

### <span data-ttu-id="4715b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4715b-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="4715b-109">Liste verknüpfter Speicherspeicher für Arbeitsbereich {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="4715b-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="4715b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4715b-110">PARAMETERS</span></span>

### <span data-ttu-id="4715b-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="4715b-111">-DataSourceType</span></span>
<span data-ttu-id="4715b-112">Datenquellentyp sollte einer von "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="4715b-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="4715b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4715b-113">-DefaultProfile</span></span>
<span data-ttu-id="4715b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4715b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4715b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4715b-115">-ResourceGroupName</span></span>
<span data-ttu-id="4715b-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4715b-116">The resource group name.</span></span>

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

### <span data-ttu-id="4715b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4715b-117">-WorkspaceName</span></span>
<span data-ttu-id="4715b-118">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4715b-118">The workspace name.</span></span>

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

### <span data-ttu-id="4715b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4715b-119">CommonParameters</span></span>
<span data-ttu-id="4715b-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4715b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4715b-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4715b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4715b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4715b-122">INPUTS</span></span>

### <span data-ttu-id="4715b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4715b-123">System.String</span></span>

## <span data-ttu-id="4715b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4715b-124">OUTPUTS</span></span>

### <span data-ttu-id="4715b-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="4715b-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="4715b-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4715b-126">NOTES</span></span>

## <span data-ttu-id="4715b-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4715b-127">RELATED LINKS</span></span>