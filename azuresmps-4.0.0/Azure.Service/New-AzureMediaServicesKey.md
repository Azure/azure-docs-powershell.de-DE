---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006207"
---
# <span data-ttu-id="0e68d-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="0e68d-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="0e68d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e68d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e68d-103">Aktualisiert Azure Media Services-Kontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="0e68d-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="0e68d-104">**Hinweis:** Diese Version ist veraltet, bitte lesen Sie die [neuere Version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="0e68d-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="0e68d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e68d-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e68d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e68d-106">DESCRIPTION</span></span>
<span data-ttu-id="0e68d-107">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0e68d-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0e68d-108">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0e68d-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0e68d-109">Das Cmdlet **New-AzureMediaServicesKey** aktualisiert den primären oder sekundären Schlüssel für das angegebene Media Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="0e68d-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="0e68d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e68d-110">EXAMPLES</span></span>

### <span data-ttu-id="0e68d-111">Beispiel 1: Aktualisieren eines Media Services-kontoschlüssels</span><span class="sxs-lookup"><span data-stu-id="0e68d-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="0e68d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e68d-112">PARAMETERS</span></span>

### <span data-ttu-id="0e68d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0e68d-113">-Force</span></span>
<span data-ttu-id="0e68d-114">Gibt an, dass die Schlüsselgenerierung nicht bestätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e68d-114">Indicates that the key generation is not confirmed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e68d-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0e68d-115">-KeyType</span></span>
<span data-ttu-id="0e68d-116">Gibt den Key-Typ der Mediendienste an; Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0e68d-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="0e68d-117">Primär</span><span class="sxs-lookup"><span data-stu-id="0e68d-117">Primary</span></span>
- <span data-ttu-id="0e68d-118">Sekundär</span><span class="sxs-lookup"><span data-stu-id="0e68d-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e68d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0e68d-119">-Name</span></span>
<span data-ttu-id="0e68d-120">Gibt den Namen des Media Services-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0e68d-120">Specifies the name of the Media Services account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e68d-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="0e68d-121">-Profile</span></span>
<span data-ttu-id="0e68d-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0e68d-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e68d-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0e68d-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e68d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e68d-124">-Confirm</span></span>
<span data-ttu-id="0e68d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e68d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e68d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e68d-126">-WhatIf</span></span>
<span data-ttu-id="0e68d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e68d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e68d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e68d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e68d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e68d-129">CommonParameters</span></span>
<span data-ttu-id="0e68d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e68d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e68d-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e68d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e68d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e68d-132">INPUTS</span></span>

## <span data-ttu-id="0e68d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e68d-133">OUTPUTS</span></span>

## <span data-ttu-id="0e68d-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e68d-134">NOTES</span></span>

## <span data-ttu-id="0e68d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e68d-135">RELATED LINKS</span></span>

[<span data-ttu-id="0e68d-136">Verwenden von Azure PowerShell für Mediendienste</span><span class="sxs-lookup"><span data-stu-id="0e68d-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


