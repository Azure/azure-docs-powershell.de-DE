---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153945"
---
# <span data-ttu-id="b2e13-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="b2e13-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="b2e13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e13-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e13-103">Dienstverknüpfung für Arbeitsbereich entfernen</span><span class="sxs-lookup"><span data-stu-id="b2e13-103">Unlink service for workspace</span></span>

## <span data-ttu-id="b2e13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2e13-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e13-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2e13-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e13-106">Dienstverknüpfung für Arbeitsbereich entfernen</span><span class="sxs-lookup"><span data-stu-id="b2e13-106">Unlink service for workspace</span></span>

## <span data-ttu-id="b2e13-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2e13-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e13-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2e13-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="b2e13-109">Verknüpfung des verknüpften Diensts für Arbeitsbereich entfernen</span><span class="sxs-lookup"><span data-stu-id="b2e13-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="b2e13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e13-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e13-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2e13-111">-AsJob</span></span>
<span data-ttu-id="b2e13-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b2e13-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2e13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e13-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e13-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2e13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e13-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b2e13-115">-LinkedServiceName</span></span>
<span data-ttu-id="b2e13-116">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b2e13-116">The Workspace name.</span></span>

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

### <span data-ttu-id="b2e13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e13-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2e13-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b2e13-118">The resource group name.</span></span>

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

### <span data-ttu-id="b2e13-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b2e13-119">-WorkspaceName</span></span>
<span data-ttu-id="b2e13-120">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b2e13-120">The Workspace name.</span></span>

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

### <span data-ttu-id="b2e13-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2e13-121">-Confirm</span></span>
<span data-ttu-id="b2e13-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2e13-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e13-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b2e13-123">-WhatIf</span></span>
<span data-ttu-id="b2e13-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2e13-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e13-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2e13-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e13-126">CommonParameters</span></span>
<span data-ttu-id="b2e13-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e13-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2e13-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e13-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2e13-129">INPUTS</span></span>

### <span data-ttu-id="b2e13-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b2e13-130">System.String</span></span>

## <span data-ttu-id="b2e13-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2e13-131">OUTPUTS</span></span>

### <span data-ttu-id="b2e13-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2e13-132">System.Boolean</span></span>

## <span data-ttu-id="b2e13-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2e13-133">NOTES</span></span>

## <span data-ttu-id="b2e13-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2e13-134">RELATED LINKS</span></span>
