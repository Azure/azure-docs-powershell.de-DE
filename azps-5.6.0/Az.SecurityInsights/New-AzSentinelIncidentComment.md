---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 0fe04e773e02a8b6b61f9c57d8316ac8936f05aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924451"
---
# <span data-ttu-id="c0d14-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="c0d14-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="c0d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d14-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d14-103">Fügen Sie einem Vorfall einen Kommentar hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0d14-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="c0d14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0d14-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d14-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0d14-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d14-106">Das **Cmdlet New-AzSentinelIncidentComment** erstellt einen Vorfallkommentar aus dem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c0d14-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="c0d14-107">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c0d14-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c0d14-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0d14-108">EXAMPLES</span></span>

### <span data-ttu-id="c0d14-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0d14-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="c0d14-110">In diesem Beispiel wird ein **IncidentComment** im angegebenen Arbeitsbereich erstellt und dann in der $IncidentComment gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c0d14-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="c0d14-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c0d14-111">PARAMETERS</span></span>

### <span data-ttu-id="c0d14-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d14-112">-DefaultProfile</span></span>
<span data-ttu-id="c0d14-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0d14-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d14-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="c0d14-114">-IncidentCommentId</span></span>
<span data-ttu-id="c0d14-115">Vorfallkommentar-ID.</span><span class="sxs-lookup"><span data-stu-id="c0d14-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="c0d14-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c0d14-116">-IncidentId</span></span>
<span data-ttu-id="c0d14-117">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="c0d14-117">Incident Id.</span></span>

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

### <span data-ttu-id="c0d14-118">-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c0d14-118">-Message</span></span>
<span data-ttu-id="c0d14-119">Meldung "Vorfall".</span><span class="sxs-lookup"><span data-stu-id="c0d14-119">Incident Message.</span></span>

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

### <span data-ttu-id="c0d14-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d14-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0d14-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c0d14-121">Resource group name.</span></span>

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

### <span data-ttu-id="c0d14-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0d14-122">-WorkspaceName</span></span>
<span data-ttu-id="c0d14-123">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="c0d14-123">Workspace Name.</span></span>

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

### <span data-ttu-id="c0d14-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0d14-124">-Confirm</span></span>
<span data-ttu-id="c0d14-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0d14-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d14-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d14-126">-WhatIf</span></span>
<span data-ttu-id="c0d14-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0d14-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0d14-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0d14-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d14-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d14-129">CommonParameters</span></span>
<span data-ttu-id="c0d14-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d14-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d14-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0d14-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d14-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0d14-132">INPUTS</span></span>

### <span data-ttu-id="c0d14-133">Keine</span><span class="sxs-lookup"><span data-stu-id="c0d14-133">None</span></span>
## <span data-ttu-id="c0d14-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0d14-134">OUTPUTS</span></span>

### <span data-ttu-id="c0d14-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="c0d14-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="c0d14-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c0d14-136">NOTES</span></span>

## <span data-ttu-id="c0d14-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c0d14-137">RELATED LINKS</span></span>
