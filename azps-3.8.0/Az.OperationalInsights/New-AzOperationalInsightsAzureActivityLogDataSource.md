---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995339"
---
# <span data-ttu-id="56925-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="56925-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="56925-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56925-102">SYNOPSIS</span></span>
<span data-ttu-id="56925-103">Das Azure-Aktivitätsprotokoll wird von einem bestimmten Abonnement erfasst.</span><span class="sxs-lookup"><span data-stu-id="56925-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="56925-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56925-104">SYNTAX</span></span>

### <span data-ttu-id="56925-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="56925-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56925-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="56925-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56925-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56925-107">DESCRIPTION</span></span>
<span data-ttu-id="56925-108">Die New-AzOperationalInsightsAzureActivityLogDataSource Protokollanalyse aktivieren, um das Azure-Aktivitätsprotokoll aus einem bestimmten Abonnement zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="56925-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="56925-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56925-109">EXAMPLES</span></span>

### <span data-ttu-id="56925-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56925-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="56925-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="56925-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="56925-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="56925-112">PARAMETERS</span></span>

### <span data-ttu-id="56925-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="56925-113">-BackfillStartTime</span></span>
<span data-ttu-id="56925-114">Sie können auswählen, dass Protokolle vor einer Woche abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="56925-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="56925-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56925-115">-DefaultProfile</span></span>
<span data-ttu-id="56925-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="56925-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56925-117">-Force</span><span class="sxs-lookup"><span data-stu-id="56925-117">-Force</span></span>
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

### <span data-ttu-id="56925-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56925-118">-Name</span></span>
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

### <span data-ttu-id="56925-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56925-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="56925-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="56925-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="56925-121">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="56925-121">-Workspace</span></span>
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

### <span data-ttu-id="56925-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56925-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="56925-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56925-123">-Confirm</span></span>
<span data-ttu-id="56925-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56925-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56925-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56925-125">-WhatIf</span></span>
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

### <span data-ttu-id="56925-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56925-126">CommonParameters</span></span>
<span data-ttu-id="56925-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56925-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56925-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56925-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56925-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56925-129">INPUTS</span></span>

### <span data-ttu-id="56925-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="56925-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="56925-131">System. String</span><span class="sxs-lookup"><span data-stu-id="56925-131">System.String</span></span>

### <span data-ttu-id="56925-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56925-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="56925-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56925-133">OUTPUTS</span></span>

### <span data-ttu-id="56925-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="56925-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="56925-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="56925-135">NOTES</span></span>

## <span data-ttu-id="56925-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56925-136">RELATED LINKS</span></span>
