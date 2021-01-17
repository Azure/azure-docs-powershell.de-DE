---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471582"
---
# <span data-ttu-id="ccdfb-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="ccdfb-101">Save-AzContext</span></span>

## <span data-ttu-id="ccdfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccdfb-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdfb-103">Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ccdfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccdfb-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdfb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccdfb-105">DESCRIPTION</span></span>
<span data-ttu-id="ccdfb-106">Das Save-AzContext cmdlet speichert die aktuellen Authentifizierungsinformationen für die Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ccdfb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ccdfb-107">EXAMPLES</span></span>

### <span data-ttu-id="ccdfb-108">Beispiel 1: Speichern des Kontexts der aktuellen Sitzung</span><span class="sxs-lookup"><span data-stu-id="ccdfb-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="ccdfb-109">In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der bereitgestellten JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="ccdfb-110">Beispiel 2: Speichern eines bestimmten Kontexts</span><span class="sxs-lookup"><span data-stu-id="ccdfb-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="ccdfb-111">In diesem Beispiel wird der azure-Kontext, der an das Cmdlet übergeben wird, in der bereitgestellten JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="ccdfb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccdfb-112">PARAMETERS</span></span>

### <span data-ttu-id="ccdfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdfb-113">-DefaultProfile</span></span>
<span data-ttu-id="ccdfb-114">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccdfb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ccdfb-115">-Force</span></span>
<span data-ttu-id="ccdfb-116">Überschreiben der vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="ccdfb-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ccdfb-117">-Path</span><span class="sxs-lookup"><span data-stu-id="ccdfb-117">-Path</span></span>
<span data-ttu-id="ccdfb-118">Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="ccdfb-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="ccdfb-119">-Profile</span></span>
<span data-ttu-id="ccdfb-120">Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="ccdfb-121">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="ccdfb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccdfb-122">-Confirm</span></span>
<span data-ttu-id="ccdfb-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccdfb-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ccdfb-124">-WhatIf</span></span>
<span data-ttu-id="ccdfb-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdfb-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccdfb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdfb-127">CommonParameters</span></span>
<span data-ttu-id="ccdfb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdfb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdfb-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdfb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdfb-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ccdfb-130">INPUTS</span></span>

### <span data-ttu-id="ccdfb-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ccdfb-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="ccdfb-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ccdfb-132">OUTPUTS</span></span>

### <span data-ttu-id="ccdfb-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ccdfb-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ccdfb-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ccdfb-134">NOTES</span></span>

## <span data-ttu-id="ccdfb-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ccdfb-135">RELATED LINKS</span></span>
