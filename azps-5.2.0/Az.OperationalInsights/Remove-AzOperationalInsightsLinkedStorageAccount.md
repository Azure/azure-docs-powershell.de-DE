---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299139"
---
# <span data-ttu-id="d2534-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2534-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d2534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2534-102">SYNOPSIS</span></span>
<span data-ttu-id="d2534-103">Löschen eines verknüpften Speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d2534-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="d2534-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2534-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2534-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2534-105">DESCRIPTION</span></span>
<span data-ttu-id="d2534-106">Löschen eines verknüpften Speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d2534-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="d2534-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2534-107">EXAMPLES</span></span>

### <span data-ttu-id="d2534-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2534-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="d2534-109">Löschen eines verknüpften Speicherkontos mit dem Typ "CustomLogs" für {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="d2534-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="d2534-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2534-110">PARAMETERS</span></span>

### <span data-ttu-id="d2534-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="d2534-111">-DataSourceType</span></span>
<span data-ttu-id="d2534-112">Der Datenquellentyp sollte einer von "CustomLogs", "AzureDatson" sein.</span><span class="sxs-lookup"><span data-stu-id="d2534-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="d2534-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2534-113">-DefaultProfile</span></span>
<span data-ttu-id="d2534-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2534-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2534-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d2534-115">-Force</span></span>
<span data-ttu-id="d2534-116">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="d2534-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d2534-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2534-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2534-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d2534-118">The resource group name.</span></span>

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

### <span data-ttu-id="d2534-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2534-119">-WorkspaceName</span></span>
<span data-ttu-id="d2534-120">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d2534-120">The workspace name.</span></span>

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

### <span data-ttu-id="d2534-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2534-121">-Confirm</span></span>
<span data-ttu-id="d2534-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2534-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2534-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2534-123">-WhatIf</span></span>
<span data-ttu-id="d2534-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2534-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2534-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2534-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2534-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2534-126">CommonParameters</span></span>
<span data-ttu-id="d2534-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2534-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2534-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2534-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2534-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2534-129">INPUTS</span></span>

### <span data-ttu-id="d2534-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d2534-130">System.String</span></span>

## <span data-ttu-id="d2534-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2534-131">OUTPUTS</span></span>

### <span data-ttu-id="d2534-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2534-132">System.Boolean</span></span>

## <span data-ttu-id="d2534-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2534-133">NOTES</span></span>

## <span data-ttu-id="d2534-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2534-134">RELATED LINKS</span></span>
