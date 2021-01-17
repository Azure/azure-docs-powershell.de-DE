---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471957"
---
# <span data-ttu-id="afa10-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="afa10-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="afa10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa10-102">SYNOPSIS</span></span>
<span data-ttu-id="afa10-103">Fügen Sie einem Vorfall einen Kommentar hinzu.</span><span class="sxs-lookup"><span data-stu-id="afa10-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="afa10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afa10-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afa10-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afa10-105">DESCRIPTION</span></span>
<span data-ttu-id="afa10-106">Das **Cmdlet "New-AzSentinelIncidentComment"** erstellt einen Vorfallkommentar aus dem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="afa10-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="afa10-107">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="afa10-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="afa10-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afa10-108">EXAMPLES</span></span>

### <span data-ttu-id="afa10-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afa10-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="afa10-110">In diesem Beispiel wird **eine IncidentComment** im angegebenen Arbeitsbereich erstellt und dann in der $IncidentComment gespeichert.</span><span class="sxs-lookup"><span data-stu-id="afa10-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="afa10-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afa10-111">PARAMETERS</span></span>

### <span data-ttu-id="afa10-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa10-112">-DefaultProfile</span></span>
<span data-ttu-id="afa10-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afa10-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa10-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="afa10-114">-IncidentCommentId</span></span>
<span data-ttu-id="afa10-115">Vorfallkommentar-ID.</span><span class="sxs-lookup"><span data-stu-id="afa10-115">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa10-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="afa10-116">-IncidentId</span></span>
<span data-ttu-id="afa10-117">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="afa10-117">Incident Id.</span></span>

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

### <span data-ttu-id="afa10-118">-Message</span><span class="sxs-lookup"><span data-stu-id="afa10-118">-Message</span></span>
<span data-ttu-id="afa10-119">Vorfallmeldung.</span><span class="sxs-lookup"><span data-stu-id="afa10-119">Incident Message.</span></span>

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

### <span data-ttu-id="afa10-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa10-120">-ResourceGroupName</span></span>
<span data-ttu-id="afa10-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="afa10-121">Resource group name.</span></span>

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

### <span data-ttu-id="afa10-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="afa10-122">-WorkspaceName</span></span>
<span data-ttu-id="afa10-123">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="afa10-123">Workspace Name.</span></span>

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

### <span data-ttu-id="afa10-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afa10-124">-Confirm</span></span>
<span data-ttu-id="afa10-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afa10-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa10-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="afa10-126">-WhatIf</span></span>
<span data-ttu-id="afa10-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afa10-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afa10-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afa10-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa10-129">CommonParameters</span></span>
<span data-ttu-id="afa10-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa10-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afa10-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa10-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afa10-132">INPUTS</span></span>

### <span data-ttu-id="afa10-133">Keine</span><span class="sxs-lookup"><span data-stu-id="afa10-133">None</span></span>
## <span data-ttu-id="afa10-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afa10-134">OUTPUTS</span></span>

### <span data-ttu-id="afa10-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="afa10-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="afa10-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="afa10-136">NOTES</span></span>

## <span data-ttu-id="afa10-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="afa10-137">RELATED LINKS</span></span>
