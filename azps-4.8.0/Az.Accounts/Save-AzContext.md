---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165401"
---
# <span data-ttu-id="47d1b-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="47d1b-101">Save-AzContext</span></span>

## <span data-ttu-id="47d1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="47d1b-103">Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="47d1b-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="47d1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47d1b-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47d1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="47d1b-106">Das Save-AzContext-Cmdlet speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="47d1b-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="47d1b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="47d1b-108">Beispiel 1: Speichern des Kontexts der aktuellen Sitzung</span><span class="sxs-lookup"><span data-stu-id="47d1b-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="47d1b-109">In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der angegebenen JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47d1b-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="47d1b-110">Beispiel 2: Speichern eines bestimmten Kontexts</span><span class="sxs-lookup"><span data-stu-id="47d1b-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="47d1b-111">In diesem Beispiel wird der Azure-Kontext, der an das Cmdlet übergeben wird, in die angegebene JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47d1b-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="47d1b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="47d1b-112">PARAMETERS</span></span>

### <span data-ttu-id="47d1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d1b-113">-DefaultProfile</span></span>
<span data-ttu-id="47d1b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="47d1b-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47d1b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47d1b-115">-Force</span></span>
<span data-ttu-id="47d1b-116">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="47d1b-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="47d1b-117">-Path</span><span class="sxs-lookup"><span data-stu-id="47d1b-117">-Path</span></span>
<span data-ttu-id="47d1b-118">Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47d1b-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="47d1b-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="47d1b-119">-Profile</span></span>
<span data-ttu-id="47d1b-120">Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="47d1b-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="47d1b-121">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.</span><span class="sxs-lookup"><span data-stu-id="47d1b-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="47d1b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47d1b-122">-Confirm</span></span>
<span data-ttu-id="47d1b-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47d1b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d1b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d1b-124">-WhatIf</span></span>
<span data-ttu-id="47d1b-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47d1b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47d1b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47d1b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d1b-127">CommonParameters</span></span>
<span data-ttu-id="47d1b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d1b-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d1b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d1b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47d1b-130">INPUTS</span></span>

### <span data-ttu-id="47d1b-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="47d1b-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="47d1b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47d1b-132">OUTPUTS</span></span>

### <span data-ttu-id="47d1b-133">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="47d1b-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="47d1b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="47d1b-134">NOTES</span></span>

## <span data-ttu-id="47d1b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47d1b-135">RELATED LINKS</span></span>
