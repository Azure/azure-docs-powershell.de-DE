---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471967"
---
# <span data-ttu-id="97374-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="97374-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="97374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97374-102">SYNOPSIS</span></span>
<span data-ttu-id="97374-103">Erstellen Sie eine Textmarke.</span><span class="sxs-lookup"><span data-stu-id="97374-103">Create a Bookmark.</span></span>

## <span data-ttu-id="97374-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97374-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97374-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97374-105">DESCRIPTION</span></span>
<span data-ttu-id="97374-106">Das **Cmdlet "New-AzSentinelBookmark"** erstellt eine Textmarke aus dem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="97374-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="97374-107">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="97374-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="97374-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97374-108">EXAMPLES</span></span>

### <span data-ttu-id="97374-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97374-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="97374-110">In diesem Beispiel wird **eine Textmarke** im angegebenen Arbeitsbereich erstellt und dann in der $Bookmark gespeichert.</span><span class="sxs-lookup"><span data-stu-id="97374-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="97374-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97374-111">PARAMETERS</span></span>

### <span data-ttu-id="97374-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="97374-112">-BookmarkId</span></span>
<span data-ttu-id="97374-113">"Lesezeichen-ID"</span><span class="sxs-lookup"><span data-stu-id="97374-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="97374-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97374-114">-DefaultProfile</span></span>
<span data-ttu-id="97374-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97374-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97374-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="97374-116">-DisplayName</span></span>
<span data-ttu-id="97374-117">Anzeigename der Textmarkeregel.</span><span class="sxs-lookup"><span data-stu-id="97374-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="97374-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="97374-118">-IncidentInfo</span></span>
<span data-ttu-id="97374-119">Vorfallinformationen als Lesezeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="97374-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97374-120">-Label</span><span class="sxs-lookup"><span data-stu-id="97374-120">-Label</span></span>
<span data-ttu-id="97374-121">Vorfallbezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="97374-121">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97374-122">-Notizen</span><span class="sxs-lookup"><span data-stu-id="97374-122">-Notes</span></span>
<span data-ttu-id="97374-123">Lesezeichen für Notizen.</span><span class="sxs-lookup"><span data-stu-id="97374-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="97374-124">-Query</span><span class="sxs-lookup"><span data-stu-id="97374-124">-Query</span></span>
<span data-ttu-id="97374-125">Lesezeichenabfrage.</span><span class="sxs-lookup"><span data-stu-id="97374-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="97374-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="97374-126">-QueryResult</span></span>
<span data-ttu-id="97374-127">Lesezeichenabfrageergebnis.</span><span class="sxs-lookup"><span data-stu-id="97374-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="97374-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97374-128">-ResourceGroupName</span></span>
<span data-ttu-id="97374-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="97374-129">Resource group name.</span></span>

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

### <span data-ttu-id="97374-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97374-130">-WorkspaceName</span></span>
<span data-ttu-id="97374-131">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="97374-131">Workspace Name.</span></span>

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

### <span data-ttu-id="97374-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97374-132">-Confirm</span></span>
<span data-ttu-id="97374-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97374-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97374-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="97374-134">-WhatIf</span></span>
<span data-ttu-id="97374-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97374-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97374-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97374-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97374-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97374-137">CommonParameters</span></span>
<span data-ttu-id="97374-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97374-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97374-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97374-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97374-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97374-140">INPUTS</span></span>

### <span data-ttu-id="97374-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="97374-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="97374-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97374-142">OUTPUTS</span></span>

### <span data-ttu-id="97374-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="97374-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="97374-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97374-144">NOTES</span></span>

## <span data-ttu-id="97374-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97374-145">RELATED LINKS</span></span>
