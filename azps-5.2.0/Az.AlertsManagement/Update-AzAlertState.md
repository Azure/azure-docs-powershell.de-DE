---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291778"
---
# <span data-ttu-id="ae09a-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="ae09a-101">Update-AzAlertState</span></span>

## <span data-ttu-id="ae09a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae09a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae09a-103">Aktualisiert den Warnungszustand</span><span class="sxs-lookup"><span data-stu-id="ae09a-103">Updates alert state</span></span>

## <span data-ttu-id="ae09a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae09a-104">SYNTAX</span></span>

### <span data-ttu-id="ae09a-105">ByAlertId (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae09a-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae09a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ae09a-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae09a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae09a-107">DESCRIPTION</span></span>
<span data-ttu-id="ae09a-108">**Das Cmdlet "Update-AzAlertState"** aktualisiert den Warnungszustand.</span><span class="sxs-lookup"><span data-stu-id="ae09a-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="ae09a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae09a-109">EXAMPLES</span></span>

### <span data-ttu-id="ae09a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae09a-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="ae09a-111">Dieses Cmdlet aktualisiert den Warnungszustand auf "Geschlossen".</span><span class="sxs-lookup"><span data-stu-id="ae09a-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="ae09a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae09a-112">PARAMETERS</span></span>

### <span data-ttu-id="ae09a-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="ae09a-113">-AlertId</span></span>
<span data-ttu-id="ae09a-114">Eindeutiger Bezeichner der Warnung/Ressourcen-ID einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="ae09a-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="ae09a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae09a-115">-DefaultProfile</span></span>
<span data-ttu-id="ae09a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae09a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae09a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae09a-117">-InputObject</span></span>
<span data-ttu-id="ae09a-118">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae09a-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="ae09a-119">-State</span><span class="sxs-lookup"><span data-stu-id="ae09a-119">-State</span></span>
<span data-ttu-id="ae09a-120">Aktualisierter Warnungszustand</span><span class="sxs-lookup"><span data-stu-id="ae09a-120">Updated Alert State</span></span>

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

### <span data-ttu-id="ae09a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae09a-121">-Confirm</span></span>
<span data-ttu-id="ae09a-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae09a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae09a-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ae09a-123">-WhatIf</span></span>
<span data-ttu-id="ae09a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae09a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae09a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae09a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae09a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae09a-126">CommonParameters</span></span>
<span data-ttu-id="ae09a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae09a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae09a-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae09a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae09a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae09a-129">INPUTS</span></span>

### <span data-ttu-id="ae09a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="ae09a-130">None</span></span>

## <span data-ttu-id="ae09a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae09a-131">OUTPUTS</span></span>

### <span data-ttu-id="ae09a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="ae09a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="ae09a-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae09a-133">NOTES</span></span>

## <span data-ttu-id="ae09a-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae09a-134">RELATED LINKS</span></span>
