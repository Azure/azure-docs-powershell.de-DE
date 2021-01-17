---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459800"
---
# <span data-ttu-id="e03fc-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e03fc-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="e03fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e03fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e03fc-103">Löschen eines verknüpften Speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e03fc-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="e03fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e03fc-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e03fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e03fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e03fc-106">Löschen eines verknüpften Speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e03fc-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="e03fc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e03fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e03fc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e03fc-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="e03fc-109">Löschen eines verknüpften Speicherkontos mit dem Typ "CustomLogs" für {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="e03fc-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="e03fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e03fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e03fc-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="e03fc-111">-DataSourceType</span></span>
<span data-ttu-id="e03fc-112">Der Datenquellentyp sollte einer von "CustomLogs", "AzureTyp" sein.</span><span class="sxs-lookup"><span data-stu-id="e03fc-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="e03fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03fc-113">-DefaultProfile</span></span>
<span data-ttu-id="e03fc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e03fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e03fc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e03fc-115">-Force</span></span>
<span data-ttu-id="e03fc-116">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="e03fc-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e03fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e03fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="e03fc-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e03fc-118">The resource group name.</span></span>

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

### <span data-ttu-id="e03fc-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e03fc-119">-WorkspaceName</span></span>
<span data-ttu-id="e03fc-120">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e03fc-120">The workspace name.</span></span>

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

### <span data-ttu-id="e03fc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e03fc-121">-Confirm</span></span>
<span data-ttu-id="e03fc-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e03fc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e03fc-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e03fc-123">-WhatIf</span></span>
<span data-ttu-id="e03fc-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e03fc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e03fc-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e03fc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e03fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03fc-126">CommonParameters</span></span>
<span data-ttu-id="e03fc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e03fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03fc-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e03fc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03fc-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e03fc-129">INPUTS</span></span>

### <span data-ttu-id="e03fc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e03fc-130">System.String</span></span>

## <span data-ttu-id="e03fc-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e03fc-131">OUTPUTS</span></span>

### <span data-ttu-id="e03fc-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e03fc-132">System.Boolean</span></span>

## <span data-ttu-id="e03fc-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e03fc-133">NOTES</span></span>

## <span data-ttu-id="e03fc-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e03fc-134">RELATED LINKS</span></span>
