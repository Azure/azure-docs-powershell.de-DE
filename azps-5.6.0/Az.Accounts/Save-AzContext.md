---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: f73ca19ffa2c68599a5244d41b39d90ebbd2835a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930443"
---
# <span data-ttu-id="12847-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="12847-101">Save-AzContext</span></span>

## <span data-ttu-id="12847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12847-102">SYNOPSIS</span></span>
<span data-ttu-id="12847-103">Speichert die aktuellen Authentifizierungsinformationen für die Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="12847-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="12847-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12847-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12847-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12847-105">DESCRIPTION</span></span>
<span data-ttu-id="12847-106">Das Save-AzContext-Cmdlet speichert die aktuellen Authentifizierungsinformationen für die Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="12847-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="12847-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12847-107">EXAMPLES</span></span>

### <span data-ttu-id="12847-108">Beispiel 1: Speichern des Kontexts der aktuellen Sitzung</span><span class="sxs-lookup"><span data-stu-id="12847-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="12847-109">In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der bereitgestellten JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12847-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="12847-110">Beispiel 2: Speichern eines bestimmten Kontexts</span><span class="sxs-lookup"><span data-stu-id="12847-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="12847-111">In diesem Beispiel wird der Azure-Kontext gespeichert, der an das Cmdlet an die bereitgestellte JSON-Datei übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="12847-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="12847-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12847-112">PARAMETERS</span></span>

### <span data-ttu-id="12847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12847-113">-DefaultProfile</span></span>
<span data-ttu-id="12847-114">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12847-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12847-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="12847-115">-Force</span></span>
<span data-ttu-id="12847-116">Überschreiben der angegebenen Datei, wenn sie vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="12847-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="12847-117">-Path</span><span class="sxs-lookup"><span data-stu-id="12847-117">-Path</span></span>
<span data-ttu-id="12847-118">Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="12847-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12847-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="12847-119">-Profile</span></span>
<span data-ttu-id="12847-120">Gibt den Azure-Kontext an, aus dem dieses Cmdlet gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="12847-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="12847-121">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext vor.</span><span class="sxs-lookup"><span data-stu-id="12847-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12847-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12847-122">-Confirm</span></span>
<span data-ttu-id="12847-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12847-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12847-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12847-124">-WhatIf</span></span>
<span data-ttu-id="12847-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12847-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12847-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12847-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12847-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12847-127">CommonParameters</span></span>
<span data-ttu-id="12847-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12847-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12847-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12847-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12847-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12847-130">INPUTS</span></span>

### <span data-ttu-id="12847-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="12847-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="12847-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12847-132">OUTPUTS</span></span>

### <span data-ttu-id="12847-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="12847-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="12847-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12847-134">NOTES</span></span>

## <span data-ttu-id="12847-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12847-135">RELATED LINKS</span></span>
