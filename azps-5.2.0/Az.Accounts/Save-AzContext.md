---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293483"
---
# <span data-ttu-id="e1649-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="e1649-101">Save-AzContext</span></span>

## <span data-ttu-id="e1649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1649-102">SYNOPSIS</span></span>
<span data-ttu-id="e1649-103">Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="e1649-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="e1649-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1649-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1649-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1649-105">DESCRIPTION</span></span>
<span data-ttu-id="e1649-106">Das Save-AzContext A0 speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="e1649-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="e1649-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1649-107">EXAMPLES</span></span>

### <span data-ttu-id="e1649-108">Beispiel 1: Speichern des Kontexts der aktuellen Sitzung</span><span class="sxs-lookup"><span data-stu-id="e1649-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="e1649-109">In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der bereitgestellten JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e1649-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="e1649-110">Beispiel 2: Speichern eines bestimmten Kontexts</span><span class="sxs-lookup"><span data-stu-id="e1649-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="e1649-111">In diesem Beispiel wird der azure-Kontext, der an das Cmdlet übergeben wird, in der bereitgestellten JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e1649-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="e1649-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1649-112">PARAMETERS</span></span>

### <span data-ttu-id="e1649-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1649-113">-DefaultProfile</span></span>
<span data-ttu-id="e1649-114">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1649-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1649-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e1649-115">-Force</span></span>
<span data-ttu-id="e1649-116">Überschreiben der vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="e1649-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="e1649-117">-Path</span><span class="sxs-lookup"><span data-stu-id="e1649-117">-Path</span></span>
<span data-ttu-id="e1649-118">Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e1649-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="e1649-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="e1649-119">-Profile</span></span>
<span data-ttu-id="e1649-120">Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e1649-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="e1649-121">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.</span><span class="sxs-lookup"><span data-stu-id="e1649-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="e1649-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1649-122">-Confirm</span></span>
<span data-ttu-id="e1649-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1649-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1649-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1649-124">-WhatIf</span></span>
<span data-ttu-id="e1649-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1649-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1649-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1649-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1649-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1649-127">CommonParameters</span></span>
<span data-ttu-id="e1649-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1649-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1649-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1649-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1649-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1649-130">INPUTS</span></span>

### <span data-ttu-id="e1649-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="e1649-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="e1649-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1649-132">OUTPUTS</span></span>

### <span data-ttu-id="e1649-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e1649-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="e1649-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1649-134">NOTES</span></span>

## <span data-ttu-id="e1649-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1649-135">RELATED LINKS</span></span>
