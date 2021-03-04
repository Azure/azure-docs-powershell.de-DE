---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: f1b920c3a67865cbed66c15bc686e3e38e3562db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931515"
---
# <span data-ttu-id="f5a6c-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a6c-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="f5a6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a6c-103">Erstellen eines verknüpften Speicherkontos für arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f5a6c-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="f5a6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5a6c-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a6c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5a6c-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a6c-106">Erstellen eines verknüpften Speicherkontos für arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f5a6c-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="f5a6c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5a6c-107">EXAMPLES</span></span>

### <span data-ttu-id="f5a6c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5a6c-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="f5a6c-109">Hinzufügen von verknüpften Speicher für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f5a6c-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="f5a6c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f5a6c-110">PARAMETERS</span></span>

### <span data-ttu-id="f5a6c-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="f5a6c-111">-DataSourceType</span></span>
<span data-ttu-id="f5a6c-112">Datenquellentyp sollte einer von "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a6c-113">-DefaultProfile</span></span>
<span data-ttu-id="f5a6c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a6c-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f5a6c-115">-Force</span></span>
<span data-ttu-id="f5a6c-116">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5a6c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-118">The resource group name.</span></span>

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

### <span data-ttu-id="f5a6c-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="f5a6c-119">-StorageAccountIds</span></span>
<span data-ttu-id="f5a6c-120">Liste der Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a6c-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5a6c-121">-WorkspaceName</span></span>
<span data-ttu-id="f5a6c-122">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-122">The workspace name.</span></span>

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

### <span data-ttu-id="f5a6c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5a6c-123">-Confirm</span></span>
<span data-ttu-id="f5a6c-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a6c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a6c-125">-WhatIf</span></span>
<span data-ttu-id="f5a6c-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a6c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a6c-128">CommonParameters</span></span>
<span data-ttu-id="f5a6c-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a6c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5a6c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a6c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5a6c-131">INPUTS</span></span>

### <span data-ttu-id="f5a6c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f5a6c-132">System.String</span></span>

## <span data-ttu-id="f5a6c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5a6c-133">OUTPUTS</span></span>

### <span data-ttu-id="f5a6c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="f5a6c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="f5a6c-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f5a6c-135">NOTES</span></span>

## <span data-ttu-id="f5a6c-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f5a6c-136">RELATED LINKS</span></span>
