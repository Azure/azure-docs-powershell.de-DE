---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165945"
---
# <span data-ttu-id="8c619-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="8c619-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="8c619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c619-102">SYNOPSIS</span></span>
<span data-ttu-id="8c619-103">Aktualisieren einer Textmarke</span><span class="sxs-lookup"><span data-stu-id="8c619-103">Update a Bookmark.</span></span>

## <span data-ttu-id="8c619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c619-104">SYNTAX</span></span>

### <span data-ttu-id="8c619-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="8c619-105">BookmarkId.</span></span> <span data-ttu-id="8c619-106">(Standard)</span><span class="sxs-lookup"><span data-stu-id="8c619-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c619-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8c619-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c619-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c619-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c619-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c619-109">DESCRIPTION</span></span>
<span data-ttu-id="8c619-110">Das **Cmdlet "Update-AzSentinelBookmark"** aktualisiert die Textmarke im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8c619-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="8c619-111">Sie können ein **Lesezeichenobjekt** als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können die erforderlichen *"BookmarkId"-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="8c619-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="8c619-112">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8c619-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8c619-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c619-113">EXAMPLES</span></span>

### <span data-ttu-id="8c619-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c619-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="8c619-115">Der Befehl aktualisiert die Textmarke durch Festlegen der *Eigenschaft "Notes".*</span><span class="sxs-lookup"><span data-stu-id="8c619-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="8c619-116">Alle anderen Vorteile bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="8c619-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="8c619-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8c619-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="8c619-118">Der erste Befehl ruft die Textmarke nach *BookmarkId* aus dem angegebenen Arbeitsbereich ab und speichert sie dann in der $Bookmark Variable.</span><span class="sxs-lookup"><span data-stu-id="8c619-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="8c619-119">Mit dem zweiten Befehl wird die Eigenschaft "Notes" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8c619-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="8c619-120">Alle anderen Vorteile bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="8c619-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="8c619-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c619-121">PARAMETERS</span></span>

### <span data-ttu-id="8c619-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="8c619-122">-BookmarkId</span></span>
<span data-ttu-id="8c619-123">"Lesezeichen-ID"</span><span class="sxs-lookup"><span data-stu-id="8c619-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c619-124">-DefaultProfile</span></span>
<span data-ttu-id="8c619-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c619-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8c619-126">-DisplayName</span></span>
<span data-ttu-id="8c619-127">Anzeigename der Textmarkeregel.</span><span class="sxs-lookup"><span data-stu-id="8c619-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="8c619-128">-IncidentInfo</span></span>
<span data-ttu-id="8c619-129">Vorfallinformationen als Lesezeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c619-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c619-130">-InputObject</span></span>
<span data-ttu-id="8c619-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="8c619-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-132">-Label</span><span class="sxs-lookup"><span data-stu-id="8c619-132">-Label</span></span>
<span data-ttu-id="8c619-133">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="8c619-133">Incident Labels.</span></span>

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

### <span data-ttu-id="8c619-134">-Notizen</span><span class="sxs-lookup"><span data-stu-id="8c619-134">-Notes</span></span>
<span data-ttu-id="8c619-135">Lesezeichen für Notizen.</span><span class="sxs-lookup"><span data-stu-id="8c619-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-136">-Query</span><span class="sxs-lookup"><span data-stu-id="8c619-136">-Query</span></span>
<span data-ttu-id="8c619-137">Lesezeichenabfrage.</span><span class="sxs-lookup"><span data-stu-id="8c619-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="8c619-138">-QueryResult</span></span>
<span data-ttu-id="8c619-139">Lesezeichenabfrageergebnis.</span><span class="sxs-lookup"><span data-stu-id="8c619-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c619-140">-ResourceGroupName</span></span>
<span data-ttu-id="8c619-141">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8c619-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c619-142">-ResourceId</span></span>
<span data-ttu-id="8c619-143">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8c619-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8c619-144">-WorkspaceName</span></span>
<span data-ttu-id="8c619-145">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="8c619-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c619-146">-Confirm</span></span>
<span data-ttu-id="8c619-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c619-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c619-148">-WhatIf</span></span>
<span data-ttu-id="8c619-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c619-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c619-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c619-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c619-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c619-151">CommonParameters</span></span>
<span data-ttu-id="8c619-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c619-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c619-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c619-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c619-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c619-154">INPUTS</span></span>

### <span data-ttu-id="8c619-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="8c619-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="8c619-156">System.String</span><span class="sxs-lookup"><span data-stu-id="8c619-156">System.String</span></span>

### <span data-ttu-id="8c619-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="8c619-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="8c619-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c619-158">OUTPUTS</span></span>

### <span data-ttu-id="8c619-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="8c619-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="8c619-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c619-160">NOTES</span></span>

## <span data-ttu-id="8c619-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c619-161">RELATED LINKS</span></span>
