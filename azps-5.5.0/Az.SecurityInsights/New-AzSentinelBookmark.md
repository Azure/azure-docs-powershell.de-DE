---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168969"
---
# <span data-ttu-id="27d94-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="27d94-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="27d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27d94-102">SYNOPSIS</span></span>
<span data-ttu-id="27d94-103">Erstellen Sie eine Textmarke.</span><span class="sxs-lookup"><span data-stu-id="27d94-103">Create a Bookmark.</span></span>

## <span data-ttu-id="27d94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27d94-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d94-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27d94-105">DESCRIPTION</span></span>
<span data-ttu-id="27d94-106">Das **Cmdlet "New-AzSentinelBookmark"** erstellt eine Textmarke aus dem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="27d94-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="27d94-107">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="27d94-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="27d94-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27d94-108">EXAMPLES</span></span>

### <span data-ttu-id="27d94-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27d94-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="27d94-110">In diesem Beispiel wird **eine Textmarke** im angegebenen Arbeitsbereich erstellt und dann in der $Bookmark gespeichert.</span><span class="sxs-lookup"><span data-stu-id="27d94-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="27d94-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27d94-111">PARAMETERS</span></span>

### <span data-ttu-id="27d94-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="27d94-112">-BookmarkId</span></span>
<span data-ttu-id="27d94-113">"Lesezeichen-ID"</span><span class="sxs-lookup"><span data-stu-id="27d94-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="27d94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d94-114">-DefaultProfile</span></span>
<span data-ttu-id="27d94-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27d94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d94-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27d94-116">-DisplayName</span></span>
<span data-ttu-id="27d94-117">Anzeigename der Textmarkeregel.</span><span class="sxs-lookup"><span data-stu-id="27d94-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="27d94-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="27d94-118">-IncidentInfo</span></span>
<span data-ttu-id="27d94-119">Vorfallinformationen als Lesezeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27d94-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="27d94-120">-Label</span><span class="sxs-lookup"><span data-stu-id="27d94-120">-Label</span></span>
<span data-ttu-id="27d94-121">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="27d94-121">Incident Labels.</span></span>

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

### <span data-ttu-id="27d94-122">-Notizen</span><span class="sxs-lookup"><span data-stu-id="27d94-122">-Notes</span></span>
<span data-ttu-id="27d94-123">Lesezeichen für Notizen.</span><span class="sxs-lookup"><span data-stu-id="27d94-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="27d94-124">-Query</span><span class="sxs-lookup"><span data-stu-id="27d94-124">-Query</span></span>
<span data-ttu-id="27d94-125">Lesezeichenabfrage.</span><span class="sxs-lookup"><span data-stu-id="27d94-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="27d94-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="27d94-126">-QueryResult</span></span>
<span data-ttu-id="27d94-127">Lesezeichenabfrageergebnis.</span><span class="sxs-lookup"><span data-stu-id="27d94-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="27d94-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d94-128">-ResourceGroupName</span></span>
<span data-ttu-id="27d94-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="27d94-129">Resource group name.</span></span>

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

### <span data-ttu-id="27d94-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27d94-130">-WorkspaceName</span></span>
<span data-ttu-id="27d94-131">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="27d94-131">Workspace Name.</span></span>

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

### <span data-ttu-id="27d94-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27d94-132">-Confirm</span></span>
<span data-ttu-id="27d94-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27d94-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27d94-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27d94-134">-WhatIf</span></span>
<span data-ttu-id="27d94-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27d94-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27d94-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27d94-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27d94-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d94-137">CommonParameters</span></span>
<span data-ttu-id="27d94-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d94-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d94-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27d94-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d94-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27d94-140">INPUTS</span></span>

### <span data-ttu-id="27d94-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="27d94-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="27d94-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27d94-142">OUTPUTS</span></span>

### <span data-ttu-id="27d94-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="27d94-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="27d94-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27d94-144">NOTES</span></span>

## <span data-ttu-id="27d94-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27d94-145">RELATED LINKS</span></span>
