---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474337"
---
# <span data-ttu-id="8e711-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8e711-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="8e711-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e711-102">SYNOPSIS</span></span>
<span data-ttu-id="8e711-103">Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="8e711-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="8e711-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e711-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8e711-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e711-105">DESCRIPTION</span></span>
<span data-ttu-id="8e711-106">Das Save-AzureRmContext-Cmdlet speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="8e711-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="8e711-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e711-107">EXAMPLES</span></span>

### <span data-ttu-id="8e711-108">Beispiel 1: Speichern des Kontexts der aktuellen Sitzung</span><span class="sxs-lookup"><span data-stu-id="8e711-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="8e711-109">In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der angegebenen JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8e711-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="8e711-110">Beispiel 2: Speichern eines bestimmten Kontexts</span><span class="sxs-lookup"><span data-stu-id="8e711-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="8e711-111">In diesem Beispiel wird der Azure-Kontext, der an das Cmdlet übergeben wird, in die angegebene JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8e711-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="8e711-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e711-112">PARAMETERS</span></span>

### <span data-ttu-id="8e711-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8e711-113">-Force</span></span>
<span data-ttu-id="8e711-114">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="8e711-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e711-115">-Path</span><span class="sxs-lookup"><span data-stu-id="8e711-115">-Path</span></span>
<span data-ttu-id="8e711-116">Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e711-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e711-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8e711-117">-Profile</span></span>
<span data-ttu-id="8e711-118">Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8e711-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="8e711-119">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.</span><span class="sxs-lookup"><span data-stu-id="8e711-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e711-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e711-120">-Confirm</span></span>
<span data-ttu-id="8e711-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e711-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e711-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e711-122">-WhatIf</span></span>
<span data-ttu-id="8e711-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e711-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e711-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e711-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8e711-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e711-125">INPUTS</span></span>

### <span data-ttu-id="8e711-126">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="8e711-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="8e711-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e711-127">OUTPUTS</span></span>

### <span data-ttu-id="8e711-128">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="8e711-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="8e711-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e711-129">NOTES</span></span>

## <span data-ttu-id="8e711-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e711-130">RELATED LINKS</span></span>

