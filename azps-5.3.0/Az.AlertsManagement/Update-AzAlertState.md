---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471556"
---
# <span data-ttu-id="25e28-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="25e28-101">Update-AzAlertState</span></span>

## <span data-ttu-id="25e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e28-102">SYNOPSIS</span></span>
<span data-ttu-id="25e28-103">Aktualisiert den Warnungszustand</span><span class="sxs-lookup"><span data-stu-id="25e28-103">Updates alert state</span></span>

## <span data-ttu-id="25e28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25e28-104">SYNTAX</span></span>

### <span data-ttu-id="25e28-105">ByAlertId (Standard)</span><span class="sxs-lookup"><span data-stu-id="25e28-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="25e28-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e28-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25e28-107">DESCRIPTION</span></span>
<span data-ttu-id="25e28-108">**Das Cmdlet "Update-AzAlertState"** aktualisiert den Warnungszustand.</span><span class="sxs-lookup"><span data-stu-id="25e28-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="25e28-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25e28-109">EXAMPLES</span></span>

### <span data-ttu-id="25e28-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25e28-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="25e28-111">Dieses Cmdlet aktualisiert den Warnungszustand auf "Geschlossen".</span><span class="sxs-lookup"><span data-stu-id="25e28-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="25e28-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e28-112">PARAMETERS</span></span>

### <span data-ttu-id="25e28-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="25e28-113">-AlertId</span></span>
<span data-ttu-id="25e28-114">Eindeutiger Bezeichner der Warnung/ResourceId einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="25e28-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="25e28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e28-115">-DefaultProfile</span></span>
<span data-ttu-id="25e28-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25e28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e28-117">-InputObject</span></span>
<span data-ttu-id="25e28-118">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="25e28-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="25e28-119">-State</span><span class="sxs-lookup"><span data-stu-id="25e28-119">-State</span></span>
<span data-ttu-id="25e28-120">Aktualisierter Warnungszustand</span><span class="sxs-lookup"><span data-stu-id="25e28-120">Updated Alert State</span></span>

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

### <span data-ttu-id="25e28-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e28-121">-Confirm</span></span>
<span data-ttu-id="25e28-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25e28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e28-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25e28-123">-WhatIf</span></span>
<span data-ttu-id="25e28-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25e28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e28-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25e28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e28-126">CommonParameters</span></span>
<span data-ttu-id="25e28-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e28-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25e28-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e28-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25e28-129">INPUTS</span></span>

### <span data-ttu-id="25e28-130">Keine</span><span class="sxs-lookup"><span data-stu-id="25e28-130">None</span></span>

## <span data-ttu-id="25e28-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25e28-131">OUTPUTS</span></span>

### <span data-ttu-id="25e28-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="25e28-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="25e28-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25e28-133">NOTES</span></span>

## <span data-ttu-id="25e28-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25e28-134">RELATED LINKS</span></span>
