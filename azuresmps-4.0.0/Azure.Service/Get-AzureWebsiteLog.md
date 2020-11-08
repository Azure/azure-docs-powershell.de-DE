---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006712"
---
# <span data-ttu-id="83d6d-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="83d6d-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="83d6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="83d6d-103">Ruft Protokolle für die angegebene Website ab.</span><span class="sxs-lookup"><span data-stu-id="83d6d-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="83d6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83d6d-104">SYNTAX</span></span>

### <span data-ttu-id="83d6d-105">Schwanz</span><span class="sxs-lookup"><span data-stu-id="83d6d-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83d6d-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="83d6d-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="83d6d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83d6d-107">DESCRIPTION</span></span>
<span data-ttu-id="83d6d-108">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="83d6d-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="83d6d-109">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="83d6d-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="83d6d-110">Ruft das Protokoll für die angegebene Website ab.</span><span class="sxs-lookup"><span data-stu-id="83d6d-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="83d6d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83d6d-111">EXAMPLES</span></span>

### <span data-ttu-id="83d6d-112">Beispiel 1: Starten des Streaming von Protokollen</span><span class="sxs-lookup"><span data-stu-id="83d6d-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="83d6d-113">In diesem Beispiel wird das Protokoll Streaming für alle Anwendungsprotokolle gestartet.</span><span class="sxs-lookup"><span data-stu-id="83d6d-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="83d6d-114">Beispiel 2: Starten des Streaming von Protokollen für HTTP-Protokolle</span><span class="sxs-lookup"><span data-stu-id="83d6d-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="83d6d-115">In diesem Beispiel wird das Protokoll Streaming für HTTP-Protokolle gestartet.</span><span class="sxs-lookup"><span data-stu-id="83d6d-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="83d6d-116">Beispiel 3: Starten des Protokoll-Streams für Fehlerprotokolle</span><span class="sxs-lookup"><span data-stu-id="83d6d-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="83d6d-117">In diesem Beispiel wird das Streaming von Protokollen gestartet und nur Fehlerprotokolle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83d6d-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="83d6d-118">Beispiel 4: Anzeigen von Anzeige Protokollen</span><span class="sxs-lookup"><span data-stu-id="83d6d-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="83d6d-119">In diesem Beispiel werden alle verfügbaren Protokollpfade auf der Website aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="83d6d-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="83d6d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="83d6d-120">PARAMETERS</span></span>

### <span data-ttu-id="83d6d-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="83d6d-121">-ListPath</span></span>
<span data-ttu-id="83d6d-122">Gibt an, ob die Protokollpfade aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d6d-123">-Nachricht</span><span class="sxs-lookup"><span data-stu-id="83d6d-123">-Message</span></span>
<span data-ttu-id="83d6d-124">Gibt eine Zeichenfolge an, die zum Filtern der Protokollnachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83d6d-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="83d6d-125">Es werden nur Protokolle abgerufen, die diese Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d6d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="83d6d-126">-Name</span></span>
<span data-ttu-id="83d6d-127">Der Name der Website.</span><span class="sxs-lookup"><span data-stu-id="83d6d-127">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d6d-128">-Path</span><span class="sxs-lookup"><span data-stu-id="83d6d-128">-Path</span></span>
<span data-ttu-id="83d6d-129">Der Pfad, aus dem das Protokoll abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="83d6d-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="83d6d-130">Standardmäßig handelt es sich um root, was bedeutet, dass alle Pfade eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="83d6d-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d6d-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="83d6d-131">-Profile</span></span>
<span data-ttu-id="83d6d-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="83d6d-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83d6d-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="83d6d-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83d6d-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="83d6d-134">-Slot</span></span>
<span data-ttu-id="83d6d-135">Gibt den Namen des Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="83d6d-135">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d6d-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="83d6d-136">-Tail</span></span>
<span data-ttu-id="83d6d-137">Gibt an, ob die Protokolle gestreamt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d6d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d6d-138">CommonParameters</span></span>
<span data-ttu-id="83d6d-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d6d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d6d-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d6d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d6d-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83d6d-141">INPUTS</span></span>

## <span data-ttu-id="83d6d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83d6d-142">OUTPUTS</span></span>

## <span data-ttu-id="83d6d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="83d6d-143">NOTES</span></span>

## <span data-ttu-id="83d6d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83d6d-144">RELATED LINKS</span></span>

[<span data-ttu-id="83d6d-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="83d6d-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="83d6d-146">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="83d6d-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="83d6d-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="83d6d-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="83d6d-148">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="83d6d-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


