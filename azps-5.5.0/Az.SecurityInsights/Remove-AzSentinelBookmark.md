---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158441"
---
# <span data-ttu-id="9bc47-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9bc47-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="9bc47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc47-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc47-103">Löschen einer Textmarke</span><span class="sxs-lookup"><span data-stu-id="9bc47-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="9bc47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bc47-104">SYNTAX</span></span>

### <span data-ttu-id="9bc47-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="9bc47-105">BookmarkId.</span></span> <span data-ttu-id="9bc47-106">(Standard)</span><span class="sxs-lookup"><span data-stu-id="9bc47-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bc47-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9bc47-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc47-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bc47-108">DESCRIPTION</span></span>
<span data-ttu-id="9bc47-109">Das **Cmdlet "Remove-AzSentinelBookmark"** löscht eine Textmarke dauerhaft aus einem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="9bc47-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="9bc47-110">Sie können ein **Lesezeichenobjekt** mithilfe des Pipelineoperators übergeben, oder Sie können die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9bc47-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="9bc47-111">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9bc47-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9bc47-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9bc47-112">EXAMPLES</span></span>

### <span data-ttu-id="9bc47-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9bc47-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="9bc47-114">Mit diesem Befehl wird die Textmarke aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="9bc47-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="9bc47-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bc47-115">PARAMETERS</span></span>

### <span data-ttu-id="9bc47-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="9bc47-116">-BookmarkId</span></span>
<span data-ttu-id="9bc47-117">"Lesezeichen-ID"</span><span class="sxs-lookup"><span data-stu-id="9bc47-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc47-118">-DefaultProfile</span></span>
<span data-ttu-id="9bc47-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bc47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc47-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bc47-120">-InputObject</span></span>
<span data-ttu-id="9bc47-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="9bc47-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc47-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bc47-122">-PassThru</span></span>
<span data-ttu-id="9bc47-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="9bc47-123">PassThru</span></span>

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

### <span data-ttu-id="9bc47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc47-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bc47-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9bc47-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc47-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9bc47-126">-WorkspaceName</span></span>
<span data-ttu-id="9bc47-127">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="9bc47-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc47-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bc47-128">-Confirm</span></span>
<span data-ttu-id="9bc47-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9bc47-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc47-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9bc47-130">-WhatIf</span></span>
<span data-ttu-id="9bc47-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bc47-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc47-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bc47-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc47-133">CommonParameters</span></span>
<span data-ttu-id="9bc47-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc47-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bc47-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc47-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9bc47-136">INPUTS</span></span>

### <span data-ttu-id="9bc47-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9bc47-137">System.String</span></span>
### <span data-ttu-id="9bc47-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9bc47-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="9bc47-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9bc47-139">OUTPUTS</span></span>

### <span data-ttu-id="9bc47-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9bc47-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="9bc47-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9bc47-141">NOTES</span></span>

## <span data-ttu-id="9bc47-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9bc47-142">RELATED LINKS</span></span>
