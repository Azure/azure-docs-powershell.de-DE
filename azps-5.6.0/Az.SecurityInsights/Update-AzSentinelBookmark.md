---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: eccb0ce5a9a92eae956c11273bf6397f20473e39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919115"
---
# <span data-ttu-id="46a66-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="46a66-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="46a66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a66-102">SYNOPSIS</span></span>
<span data-ttu-id="46a66-103">Aktualisieren einer Textmarke</span><span class="sxs-lookup"><span data-stu-id="46a66-103">Update a Bookmark.</span></span>

## <span data-ttu-id="46a66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46a66-104">SYNTAX</span></span>

### <span data-ttu-id="46a66-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="46a66-105">BookmarkId.</span></span> <span data-ttu-id="46a66-106">(Standard)</span><span class="sxs-lookup"><span data-stu-id="46a66-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a66-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="46a66-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a66-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a66-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a66-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46a66-109">DESCRIPTION</span></span>
<span data-ttu-id="46a66-110">Das **Cmdlet Update-AzSentinelBookmark aktualisiert** die Textmarke im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="46a66-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="46a66-111">Sie können ein **Bookmark-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben oder alternativ die erforderlichen *BookmarkId-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="46a66-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="46a66-112">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="46a66-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="46a66-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46a66-113">EXAMPLES</span></span>

### <span data-ttu-id="46a66-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46a66-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="46a66-115">Der Befehl aktualisiert die Textmarke durch Festlegen der *Notes-Eigenschaft.*</span><span class="sxs-lookup"><span data-stu-id="46a66-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="46a66-116">Alle anderen Propreties bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="46a66-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="46a66-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="46a66-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="46a66-118">Der erste Befehl ruft die Bookmark by *BookmarkId* aus dem angegebenen Arbeitsbereich ab und speichert sie dann in der $Bookmark Variable.</span><span class="sxs-lookup"><span data-stu-id="46a66-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="46a66-119">Mit dem zweiten Befehl wird die Notes-Eigenschaft aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46a66-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="46a66-120">Alle anderen Propreties bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="46a66-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="46a66-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46a66-121">PARAMETERS</span></span>

### <span data-ttu-id="46a66-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="46a66-122">-BookmarkId</span></span>
<span data-ttu-id="46a66-123">Lesezeichen-ID,</span><span class="sxs-lookup"><span data-stu-id="46a66-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="46a66-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a66-124">-DefaultProfile</span></span>
<span data-ttu-id="46a66-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46a66-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a66-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="46a66-126">-DisplayName</span></span>
<span data-ttu-id="46a66-127">Anzeigename der Lesezeichenregel.</span><span class="sxs-lookup"><span data-stu-id="46a66-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="46a66-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="46a66-128">-IncidentInfo</span></span>
<span data-ttu-id="46a66-129">Vorfallinformationen mit lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="46a66-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="46a66-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46a66-130">-InputObject</span></span>
<span data-ttu-id="46a66-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="46a66-131">InputObject.</span></span>

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

### <span data-ttu-id="46a66-132">-Label</span><span class="sxs-lookup"><span data-stu-id="46a66-132">-Label</span></span>
<span data-ttu-id="46a66-133">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="46a66-133">Incident Labels.</span></span>

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

### <span data-ttu-id="46a66-134">-Notizen</span><span class="sxs-lookup"><span data-stu-id="46a66-134">-Notes</span></span>
<span data-ttu-id="46a66-135">Lesezeichen für Notizen.</span><span class="sxs-lookup"><span data-stu-id="46a66-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="46a66-136">-Query</span><span class="sxs-lookup"><span data-stu-id="46a66-136">-Query</span></span>
<span data-ttu-id="46a66-137">Lesezeichenabfrage.</span><span class="sxs-lookup"><span data-stu-id="46a66-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="46a66-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="46a66-138">-QueryResult</span></span>
<span data-ttu-id="46a66-139">Abfrageergebnis mit Textmarken versehen.</span><span class="sxs-lookup"><span data-stu-id="46a66-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="46a66-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a66-140">-ResourceGroupName</span></span>
<span data-ttu-id="46a66-141">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46a66-141">Resource group name.</span></span>

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

### <span data-ttu-id="46a66-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a66-142">-ResourceId</span></span>
<span data-ttu-id="46a66-143">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="46a66-143">Resource Id.</span></span>

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

### <span data-ttu-id="46a66-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46a66-144">-WorkspaceName</span></span>
<span data-ttu-id="46a66-145">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="46a66-145">Workspace Name.</span></span>

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

### <span data-ttu-id="46a66-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46a66-146">-Confirm</span></span>
<span data-ttu-id="46a66-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46a66-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a66-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a66-148">-WhatIf</span></span>
<span data-ttu-id="46a66-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46a66-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a66-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46a66-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a66-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a66-151">CommonParameters</span></span>
<span data-ttu-id="46a66-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a66-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a66-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46a66-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a66-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46a66-154">INPUTS</span></span>

### <span data-ttu-id="46a66-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="46a66-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="46a66-156">System.String</span><span class="sxs-lookup"><span data-stu-id="46a66-156">System.String</span></span>

### <span data-ttu-id="46a66-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="46a66-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="46a66-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46a66-158">OUTPUTS</span></span>

### <span data-ttu-id="46a66-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="46a66-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="46a66-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46a66-160">NOTES</span></span>

## <span data-ttu-id="46a66-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46a66-161">RELATED LINKS</span></span>
