---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296525"
---
# <span data-ttu-id="70286-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70286-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="70286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70286-102">SYNOPSIS</span></span>
<span data-ttu-id="70286-103">Festlegen eines verknüpften Speicherkontos für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="70286-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="70286-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70286-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70286-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70286-105">DESCRIPTION</span></span>
<span data-ttu-id="70286-106">Festlegen eines verknüpften Speicherkontos für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="70286-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="70286-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70286-107">EXAMPLES</span></span>

### <span data-ttu-id="70286-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70286-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="70286-109">Festlegen des verknüpften Speichers für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="70286-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="70286-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70286-110">PARAMETERS</span></span>

### <span data-ttu-id="70286-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="70286-111">-DataSourceType</span></span>
<span data-ttu-id="70286-112">Der Datenquellentyp sollte einer von "CustomLogs", "AzureDatson" sein.</span><span class="sxs-lookup"><span data-stu-id="70286-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="70286-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70286-113">-DefaultProfile</span></span>
<span data-ttu-id="70286-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70286-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70286-115">-Force</span><span class="sxs-lookup"><span data-stu-id="70286-115">-Force</span></span>
<span data-ttu-id="70286-116">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="70286-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="70286-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70286-117">-ResourceGroupName</span></span>
<span data-ttu-id="70286-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70286-118">The resource group name.</span></span>

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

### <span data-ttu-id="70286-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="70286-119">-StorageAccountIds</span></span>
<span data-ttu-id="70286-120">Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="70286-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="70286-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="70286-121">-WorkspaceName</span></span>
<span data-ttu-id="70286-122">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="70286-122">The workspace name.</span></span>

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

### <span data-ttu-id="70286-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70286-123">-Confirm</span></span>
<span data-ttu-id="70286-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70286-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70286-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70286-125">-WhatIf</span></span>
<span data-ttu-id="70286-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70286-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70286-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70286-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70286-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70286-128">CommonParameters</span></span>
<span data-ttu-id="70286-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70286-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70286-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70286-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70286-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70286-131">INPUTS</span></span>

### <span data-ttu-id="70286-132">System.String</span><span class="sxs-lookup"><span data-stu-id="70286-132">System.String</span></span>

## <span data-ttu-id="70286-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70286-133">OUTPUTS</span></span>

### <span data-ttu-id="70286-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="70286-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="70286-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70286-135">NOTES</span></span>

## <span data-ttu-id="70286-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70286-136">RELATED LINKS</span></span>
