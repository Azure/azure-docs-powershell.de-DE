---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 1ab5abc4af394647fd1438ed79cebb739daaca94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935432"
---
# <span data-ttu-id="76dbb-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="76dbb-101">Update-AzAlertState</span></span>

## <span data-ttu-id="76dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="76dbb-103">Aktualisierungsbenachrichtigungszustand</span><span class="sxs-lookup"><span data-stu-id="76dbb-103">Updates alert state</span></span>

## <span data-ttu-id="76dbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76dbb-104">SYNTAX</span></span>

### <span data-ttu-id="76dbb-105">ByAlertId (Standard)</span><span class="sxs-lookup"><span data-stu-id="76dbb-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76dbb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76dbb-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76dbb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76dbb-107">DESCRIPTION</span></span>
<span data-ttu-id="76dbb-108">**Update-AzAlertState-Cmdlet** aktualisiert den Benachrichtigungszustand.</span><span class="sxs-lookup"><span data-stu-id="76dbb-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="76dbb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76dbb-109">EXAMPLES</span></span>

### <span data-ttu-id="76dbb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76dbb-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="76dbb-111">Dieses Cmdlet aktualisiert den Benachrichtigungszustand auf Geschlossen.</span><span class="sxs-lookup"><span data-stu-id="76dbb-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="76dbb-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="76dbb-112">PARAMETERS</span></span>

### <span data-ttu-id="76dbb-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="76dbb-113">-AlertId</span></span>
<span data-ttu-id="76dbb-114">Eindeutiger Bezeichner der Warnung /ResourceId der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="76dbb-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76dbb-115">-DefaultProfile</span></span>
<span data-ttu-id="76dbb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76dbb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76dbb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76dbb-117">-InputObject</span></span>
<span data-ttu-id="76dbb-118">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="76dbb-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76dbb-119">-State</span><span class="sxs-lookup"><span data-stu-id="76dbb-119">-State</span></span>
<span data-ttu-id="76dbb-120">Aktualisierter Warnungszustand</span><span class="sxs-lookup"><span data-stu-id="76dbb-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dbb-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76dbb-121">-Confirm</span></span>
<span data-ttu-id="76dbb-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76dbb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76dbb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76dbb-123">-WhatIf</span></span>
<span data-ttu-id="76dbb-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76dbb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76dbb-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76dbb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76dbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76dbb-126">CommonParameters</span></span>
<span data-ttu-id="76dbb-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76dbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76dbb-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76dbb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76dbb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76dbb-129">INPUTS</span></span>

### <span data-ttu-id="76dbb-130">Keine</span><span class="sxs-lookup"><span data-stu-id="76dbb-130">None</span></span>

## <span data-ttu-id="76dbb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76dbb-131">OUTPUTS</span></span>

### <span data-ttu-id="76dbb-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="76dbb-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="76dbb-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="76dbb-133">NOTES</span></span>

## <span data-ttu-id="76dbb-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="76dbb-134">RELATED LINKS</span></span>
