---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178287"
---
# <span data-ttu-id="97074-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97074-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="97074-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97074-102">SYNOPSIS</span></span>
<span data-ttu-id="97074-103">Erstellen eines verknüpften speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="97074-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="97074-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97074-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97074-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97074-105">DESCRIPTION</span></span>
<span data-ttu-id="97074-106">Erstellen eines verknüpften speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="97074-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="97074-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97074-107">EXAMPLES</span></span>

### <span data-ttu-id="97074-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97074-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="97074-109">Hinzufügen eines verknüpften Speichers für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="97074-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="97074-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="97074-110">PARAMETERS</span></span>

### <span data-ttu-id="97074-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="97074-111">-DataSourceType</span></span>
<span data-ttu-id="97074-112">Der Datenquellentyp sollte "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="97074-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="97074-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97074-113">-DefaultProfile</span></span>
<span data-ttu-id="97074-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97074-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97074-115">-Force</span><span class="sxs-lookup"><span data-stu-id="97074-115">-Force</span></span>
<span data-ttu-id="97074-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="97074-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="97074-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97074-117">-ResourceGroupName</span></span>
<span data-ttu-id="97074-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97074-118">The resource group name.</span></span>

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

### <span data-ttu-id="97074-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="97074-119">-StorageAccountIds</span></span>
<span data-ttu-id="97074-120">Liste der Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="97074-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="97074-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97074-121">-WorkspaceName</span></span>
<span data-ttu-id="97074-122">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="97074-122">The workspace name.</span></span>

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

### <span data-ttu-id="97074-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="97074-123">-Confirm</span></span>
<span data-ttu-id="97074-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97074-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97074-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97074-125">-WhatIf</span></span>
<span data-ttu-id="97074-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97074-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97074-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97074-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97074-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97074-128">CommonParameters</span></span>
<span data-ttu-id="97074-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97074-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97074-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97074-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97074-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97074-131">INPUTS</span></span>

### <span data-ttu-id="97074-132">System. String</span><span class="sxs-lookup"><span data-stu-id="97074-132">System.String</span></span>

## <span data-ttu-id="97074-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97074-133">OUTPUTS</span></span>

### <span data-ttu-id="97074-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="97074-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="97074-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="97074-135">NOTES</span></span>

## <span data-ttu-id="97074-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97074-136">RELATED LINKS</span></span>
