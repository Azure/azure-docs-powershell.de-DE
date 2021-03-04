---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 8e4dd13b93a0aadf8c69325bc6d79a2a1b3e1359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937896"
---
# <span data-ttu-id="2250f-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2250f-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2250f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2250f-102">SYNOPSIS</span></span>
<span data-ttu-id="2250f-103">Löschen des verknüpften Speicherkontos für arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="2250f-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="2250f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2250f-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2250f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2250f-105">DESCRIPTION</span></span>
<span data-ttu-id="2250f-106">Löschen des verknüpften Speicherkontos für arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="2250f-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="2250f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2250f-107">EXAMPLES</span></span>

### <span data-ttu-id="2250f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2250f-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="2250f-109">Löschen des verknüpften Speicherkontos mit dem Typ "CustomLogs" für {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="2250f-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="2250f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2250f-110">PARAMETERS</span></span>

### <span data-ttu-id="2250f-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="2250f-111">-DataSourceType</span></span>
<span data-ttu-id="2250f-112">Datenquellentyp sollte einer von "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="2250f-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="2250f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2250f-113">-DefaultProfile</span></span>
<span data-ttu-id="2250f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2250f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2250f-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2250f-115">-Force</span></span>
<span data-ttu-id="2250f-116">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="2250f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2250f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2250f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2250f-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2250f-118">The resource group name.</span></span>

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

### <span data-ttu-id="2250f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2250f-119">-WorkspaceName</span></span>
<span data-ttu-id="2250f-120">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2250f-120">The workspace name.</span></span>

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

### <span data-ttu-id="2250f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2250f-121">-Confirm</span></span>
<span data-ttu-id="2250f-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2250f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2250f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2250f-123">-WhatIf</span></span>
<span data-ttu-id="2250f-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2250f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2250f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2250f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2250f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2250f-126">CommonParameters</span></span>
<span data-ttu-id="2250f-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2250f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2250f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2250f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2250f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2250f-129">INPUTS</span></span>

### <span data-ttu-id="2250f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2250f-130">System.String</span></span>

## <span data-ttu-id="2250f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2250f-131">OUTPUTS</span></span>

### <span data-ttu-id="2250f-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2250f-132">System.Boolean</span></span>

## <span data-ttu-id="2250f-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2250f-133">NOTES</span></span>

## <span data-ttu-id="2250f-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2250f-134">RELATED LINKS</span></span>
