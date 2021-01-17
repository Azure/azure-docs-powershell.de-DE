---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356641"
---
# <span data-ttu-id="d5786-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="d5786-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="d5786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5786-102">SYNOPSIS</span></span>
<span data-ttu-id="d5786-103">Sammeln Sie das Azure-Aktivitätsprotokoll aus einem bestimmten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5786-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="d5786-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5786-104">SYNTAX</span></span>

### <span data-ttu-id="d5786-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5786-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5786-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5786-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5786-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5786-107">DESCRIPTION</span></span>
<span data-ttu-id="d5786-108">Die New-AzOperationalInsightsAzureActivityLogDataSource die Protokollanalyse zum Erfassen des Azure-Aktivitätsprotokolls aus einem bestimmten Abonnement aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d5786-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="d5786-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5786-109">EXAMPLES</span></span>

### <span data-ttu-id="d5786-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5786-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d5786-111">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="d5786-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d5786-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5786-112">PARAMETERS</span></span>

### <span data-ttu-id="d5786-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="d5786-113">-BackfillStartTime</span></span>
<span data-ttu-id="d5786-114">Sie können auswählen, dass Protokolle aus einer Woche ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="d5786-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5786-115">-DefaultProfile</span></span>
<span data-ttu-id="d5786-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d5786-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d5786-117">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d5786-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5786-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5786-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d5786-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5786-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5786-123">-Confirm</span></span>
<span data-ttu-id="d5786-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5786-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5786-125">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5786-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5786-126">CommonParameters</span></span>
<span data-ttu-id="d5786-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5786-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5786-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5786-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5786-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5786-129">INPUTS</span></span>

### <span data-ttu-id="d5786-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5786-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d5786-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d5786-131">System.String</span></span>

### <span data-ttu-id="d5786-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d5786-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="d5786-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5786-133">OUTPUTS</span></span>

### <span data-ttu-id="d5786-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d5786-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d5786-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5786-135">NOTES</span></span>

## <span data-ttu-id="d5786-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5786-136">RELATED LINKS</span></span>
