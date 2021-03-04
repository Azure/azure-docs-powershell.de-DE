---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 8a78fc36e13360babc43b512dccee80550b3fbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937931"
---
# <span data-ttu-id="bc00c-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="bc00c-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="bc00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc00c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc00c-103">Entfernen des Verknüpfungsdiensts für arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bc00c-103">Unlink service for workspace</span></span>

## <span data-ttu-id="bc00c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc00c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc00c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc00c-105">DESCRIPTION</span></span>
<span data-ttu-id="bc00c-106">Entfernen des Verknüpfungsdiensts für arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bc00c-106">Unlink service for workspace</span></span>

## <span data-ttu-id="bc00c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc00c-107">EXAMPLES</span></span>

### <span data-ttu-id="bc00c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc00c-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="bc00c-109">Verknüpfung des verknüpften Diensts für Arbeitsbereich wird nicht mehr verknüpft</span><span class="sxs-lookup"><span data-stu-id="bc00c-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="bc00c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bc00c-110">PARAMETERS</span></span>

### <span data-ttu-id="bc00c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc00c-111">-AsJob</span></span>
<span data-ttu-id="bc00c-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bc00c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc00c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc00c-113">-DefaultProfile</span></span>
<span data-ttu-id="bc00c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc00c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc00c-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="bc00c-115">-LinkedServiceName</span></span>
<span data-ttu-id="bc00c-116">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="bc00c-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc00c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc00c-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc00c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc00c-118">The resource group name.</span></span>

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

### <span data-ttu-id="bc00c-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bc00c-119">-WorkspaceName</span></span>
<span data-ttu-id="bc00c-120">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="bc00c-120">The Workspace name.</span></span>

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

### <span data-ttu-id="bc00c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc00c-121">-Confirm</span></span>
<span data-ttu-id="bc00c-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc00c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc00c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc00c-123">-WhatIf</span></span>
<span data-ttu-id="bc00c-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc00c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc00c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc00c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc00c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc00c-126">CommonParameters</span></span>
<span data-ttu-id="bc00c-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc00c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc00c-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc00c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc00c-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc00c-129">INPUTS</span></span>

### <span data-ttu-id="bc00c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bc00c-130">System.String</span></span>

## <span data-ttu-id="bc00c-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc00c-131">OUTPUTS</span></span>

### <span data-ttu-id="bc00c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc00c-132">System.Boolean</span></span>

## <span data-ttu-id="bc00c-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bc00c-133">NOTES</span></span>

## <span data-ttu-id="bc00c-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bc00c-134">RELATED LINKS</span></span>
