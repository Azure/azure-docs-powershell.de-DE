---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475205"
---
# <span data-ttu-id="a3828-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a3828-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="a3828-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3828-102">SYNOPSIS</span></span>
<span data-ttu-id="a3828-103">Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a3828-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="a3828-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3828-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3828-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3828-105">DESCRIPTION</span></span>
<span data-ttu-id="a3828-106">Das Save-AzureRmProfile-Cmdlet speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a3828-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="a3828-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3828-107">EXAMPLES</span></span>

### <span data-ttu-id="a3828-108">Beispiel 1: Speichern des Profils der aktuellen Sitzung</span><span class="sxs-lookup"><span data-stu-id="a3828-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="a3828-109">In diesem Beispiel wird das Azure-Profil der aktuellen Sitzung in der angegebenen JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a3828-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="a3828-110">Beispiel 2: Speichern eines angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="a3828-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="a3828-111">In diesem Beispiel wird das Azure-Profil, das an das Cmdlet übergeben wird, in die angegebene JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a3828-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="a3828-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3828-112">PARAMETERS</span></span>

### <span data-ttu-id="a3828-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a3828-113">-Force</span></span>
<span data-ttu-id="a3828-114">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="a3828-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="a3828-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a3828-115">-Path</span></span>
<span data-ttu-id="a3828-116">Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3828-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3828-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a3828-117">-Profile</span></span>
<span data-ttu-id="a3828-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a3828-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3828-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a3828-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3828-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3828-120">-Confirm</span></span>
<span data-ttu-id="a3828-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3828-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3828-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3828-122">-WhatIf</span></span>
<span data-ttu-id="a3828-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3828-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3828-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3828-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3828-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3828-125">CommonParameters</span></span>
<span data-ttu-id="a3828-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3828-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3828-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3828-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3828-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3828-128">INPUTS</span></span>

## <span data-ttu-id="a3828-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3828-129">OUTPUTS</span></span>

### <span data-ttu-id="a3828-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a3828-130">PSAzureProfile</span></span>

## <span data-ttu-id="a3828-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3828-131">NOTES</span></span>

## <span data-ttu-id="a3828-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3828-132">RELATED LINKS</span></span>

[<span data-ttu-id="a3828-133">SELECT-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="a3828-133">Select-AzureRMProfile</span></span>]()

