---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930792"
---
# <span data-ttu-id="46b79-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="46b79-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="46b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b79-102">SYNOPSIS</span></span>
<span data-ttu-id="46b79-103">Erstellen sie eine Textmarke.</span><span class="sxs-lookup"><span data-stu-id="46b79-103">Create a Bookmark.</span></span>

## <span data-ttu-id="46b79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46b79-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b79-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46b79-105">DESCRIPTION</span></span>
<span data-ttu-id="46b79-106">Das **Cmdlet New-AzSentinelBookmark erstellt** eine Textmarke aus dem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="46b79-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="46b79-107">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="46b79-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="46b79-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46b79-108">EXAMPLES</span></span>

### <span data-ttu-id="46b79-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46b79-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="46b79-110">In diesem Beispiel wird eine **Textmarke** im angegebenen Arbeitsbereich erstellt und dann in der $Bookmark gespeichert.</span><span class="sxs-lookup"><span data-stu-id="46b79-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="46b79-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46b79-111">PARAMETERS</span></span>

### <span data-ttu-id="46b79-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="46b79-112">-BookmarkId</span></span>
<span data-ttu-id="46b79-113">Lesezeichen-ID,</span><span class="sxs-lookup"><span data-stu-id="46b79-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="46b79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b79-114">-DefaultProfile</span></span>
<span data-ttu-id="46b79-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46b79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b79-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="46b79-116">-DisplayName</span></span>
<span data-ttu-id="46b79-117">Anzeigename der Lesezeichenregel.</span><span class="sxs-lookup"><span data-stu-id="46b79-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="46b79-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="46b79-118">-IncidentInfo</span></span>
<span data-ttu-id="46b79-119">Vorfallinformationen mit lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="46b79-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="46b79-120">-Label</span><span class="sxs-lookup"><span data-stu-id="46b79-120">-Label</span></span>
<span data-ttu-id="46b79-121">Vorfallbeschriftungen.</span><span class="sxs-lookup"><span data-stu-id="46b79-121">Incident Labels.</span></span>

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

### <span data-ttu-id="46b79-122">-Notizen</span><span class="sxs-lookup"><span data-stu-id="46b79-122">-Notes</span></span>
<span data-ttu-id="46b79-123">Lesezeichen für Notizen.</span><span class="sxs-lookup"><span data-stu-id="46b79-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="46b79-124">-Query</span><span class="sxs-lookup"><span data-stu-id="46b79-124">-Query</span></span>
<span data-ttu-id="46b79-125">Lesezeichenabfrage.</span><span class="sxs-lookup"><span data-stu-id="46b79-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="46b79-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="46b79-126">-QueryResult</span></span>
<span data-ttu-id="46b79-127">Abfrageergebnis mit Textmarken versehen.</span><span class="sxs-lookup"><span data-stu-id="46b79-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="46b79-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b79-128">-ResourceGroupName</span></span>
<span data-ttu-id="46b79-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46b79-129">Resource group name.</span></span>

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

### <span data-ttu-id="46b79-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46b79-130">-WorkspaceName</span></span>
<span data-ttu-id="46b79-131">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="46b79-131">Workspace Name.</span></span>

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

### <span data-ttu-id="46b79-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46b79-132">-Confirm</span></span>
<span data-ttu-id="46b79-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46b79-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b79-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b79-134">-WhatIf</span></span>
<span data-ttu-id="46b79-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46b79-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46b79-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46b79-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b79-137">CommonParameters</span></span>
<span data-ttu-id="46b79-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b79-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46b79-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b79-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46b79-140">INPUTS</span></span>

### <span data-ttu-id="46b79-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="46b79-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="46b79-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46b79-142">OUTPUTS</span></span>

### <span data-ttu-id="46b79-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="46b79-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="46b79-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46b79-144">NOTES</span></span>

## <span data-ttu-id="46b79-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46b79-145">RELATED LINKS</span></span>
