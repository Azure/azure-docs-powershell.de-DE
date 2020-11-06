---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 654663e9fdc44270266aa2872b7deb939be93e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482182"
---
# <span data-ttu-id="923d5-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="923d5-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="923d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="923d5-102">SYNOPSIS</span></span>
<span data-ttu-id="923d5-103">Das Azure-Aktivitätsprotokoll wird von einem bestimmten Abonnement erfasst.</span><span class="sxs-lookup"><span data-stu-id="923d5-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="923d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="923d5-104">SYNTAX</span></span>

### <span data-ttu-id="923d5-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="923d5-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="923d5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="923d5-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="923d5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="923d5-107">DESCRIPTION</span></span>
<span data-ttu-id="923d5-108">Die New-AzureRmOperationalInsightsAzureActivityLogDataSource Protokollanalyse aktivieren, um das Azure-Aktivitätsprotokoll aus einem bestimmten Abonnement zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="923d5-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="923d5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="923d5-109">EXAMPLES</span></span>

### <span data-ttu-id="923d5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="923d5-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="923d5-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="923d5-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="923d5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="923d5-112">PARAMETERS</span></span>

### <span data-ttu-id="923d5-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="923d5-113">-BackfillStartTime</span></span>
<span data-ttu-id="923d5-114">Sie können auswählen, dass Protokolle vor einer Woche abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="923d5-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="923d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923d5-115">-DefaultProfile</span></span>
<span data-ttu-id="923d5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="923d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923d5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="923d5-117">-Force</span></span>
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

### <span data-ttu-id="923d5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="923d5-118">-Name</span></span>
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

### <span data-ttu-id="923d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923d5-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="923d5-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="923d5-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="923d5-121">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="923d5-121">-Workspace</span></span>
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

### <span data-ttu-id="923d5-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="923d5-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="923d5-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="923d5-123">-Confirm</span></span>
<span data-ttu-id="923d5-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="923d5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="923d5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="923d5-125">-WhatIf</span></span>
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

### <span data-ttu-id="923d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923d5-126">CommonParameters</span></span>
<span data-ttu-id="923d5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923d5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="923d5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923d5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="923d5-129">INPUTS</span></span>

### <span data-ttu-id="923d5-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="923d5-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="923d5-131">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="923d5-131">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="923d5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="923d5-132">System.String</span></span>

### <span data-ttu-id="923d5-133">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="923d5-133">System.DateTimeOffset</span></span>

## <span data-ttu-id="923d5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="923d5-134">OUTPUTS</span></span>

### <span data-ttu-id="923d5-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="923d5-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="923d5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="923d5-136">NOTES</span></span>

## <span data-ttu-id="923d5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="923d5-137">RELATED LINKS</span></span>
