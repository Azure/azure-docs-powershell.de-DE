---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178285"
---
# <span data-ttu-id="e8c0b-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8c0b-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="e8c0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c0b-103">Löschen eines verknüpften speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e8c0b-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="e8c0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8c0b-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8c0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c0b-106">Löschen eines verknüpften speicherkontos für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e8c0b-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="e8c0b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8c0b-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c0b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8c0b-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="e8c0b-109">Löschen eines verknüpften speicherkontos mit dem Typ "CustomLogs" für {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="e8c0b-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="e8c0b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8c0b-110">PARAMETERS</span></span>

### <span data-ttu-id="e8c0b-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="e8c0b-111">-DataSourceType</span></span>
<span data-ttu-id="e8c0b-112">Der Datenquellentyp sollte "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="e8c0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c0b-113">-DefaultProfile</span></span>
<span data-ttu-id="e8c0b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8c0b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8c0b-115">-Force</span></span>
<span data-ttu-id="e8c0b-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e8c0b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c0b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8c0b-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-118">The resource group name.</span></span>

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

### <span data-ttu-id="e8c0b-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e8c0b-119">-WorkspaceName</span></span>
<span data-ttu-id="e8c0b-120">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-120">The workspace name.</span></span>

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

### <span data-ttu-id="e8c0b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8c0b-121">-Confirm</span></span>
<span data-ttu-id="e8c0b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c0b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c0b-123">-WhatIf</span></span>
<span data-ttu-id="e8c0b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c0b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c0b-126">CommonParameters</span></span>
<span data-ttu-id="e8c0b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c0b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8c0b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c0b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8c0b-129">INPUTS</span></span>

### <span data-ttu-id="e8c0b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8c0b-130">System.String</span></span>

## <span data-ttu-id="e8c0b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8c0b-131">OUTPUTS</span></span>

### <span data-ttu-id="e8c0b-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8c0b-132">System.Boolean</span></span>

## <span data-ttu-id="e8c0b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8c0b-133">NOTES</span></span>

## <span data-ttu-id="e8c0b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8c0b-134">RELATED LINKS</span></span>
