---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006201"
---
# <span data-ttu-id="38d98-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="38d98-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="38d98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38d98-102">SYNOPSIS</span></span>
<span data-ttu-id="38d98-103">Uploads oder Importieren eines Azure RemoteApp-Vorlagenbilds</span><span class="sxs-lookup"><span data-stu-id="38d98-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="38d98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38d98-104">SYNTAX</span></span>

### <span data-ttu-id="38d98-105">UploadLocalVhd (Standard)</span><span class="sxs-lookup"><span data-stu-id="38d98-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="38d98-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="38d98-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="38d98-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38d98-107">DESCRIPTION</span></span>
<span data-ttu-id="38d98-108">Mit dem Cmdlet **New-AzureRemoteAppTemplateImage** wird ein Azure RemoteApp-Vorlagenbild hochgeladen oder importiert.</span><span class="sxs-lookup"><span data-stu-id="38d98-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="38d98-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38d98-109">EXAMPLES</span></span>

### <span data-ttu-id="38d98-110">Beispiel 1: Hochladen einer VHD-Datei zum Erstellen eines Vorlagenbilds</span><span class="sxs-lookup"><span data-stu-id="38d98-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="38d98-111">Mit diesem Befehl wird C:\RemoteAppImages\ContosoApps.VHD zum Erstellen eines Vorlagenbilds mit dem Namen ContosoApps im Nordeuropa-Rechenzentrum hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="38d98-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="38d98-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="38d98-112">PARAMETERS</span></span>

### <span data-ttu-id="38d98-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="38d98-113">-AzureVmImageName</span></span>
<span data-ttu-id="38d98-114">Gibt den Namen eines Azure-virtuellen Computers an, der als Vorlagenbild verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38d98-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d98-115">-Bildname</span><span class="sxs-lookup"><span data-stu-id="38d98-115">-ImageName</span></span>
<span data-ttu-id="38d98-116">Gibt den Namen eines Azure RemoteApp-Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="38d98-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d98-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="38d98-117">-Location</span></span>
<span data-ttu-id="38d98-118">Gibt den Azure-Bereich des Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="38d98-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d98-119">-Path</span><span class="sxs-lookup"><span data-stu-id="38d98-119">-Path</span></span>
<span data-ttu-id="38d98-120">Gibt den Dateipfad des Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="38d98-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d98-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="38d98-121">-Profile</span></span>
<span data-ttu-id="38d98-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="38d98-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38d98-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="38d98-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38d98-124">-Resume</span><span class="sxs-lookup"><span data-stu-id="38d98-124">-Resume</span></span>
<span data-ttu-id="38d98-125">Gibt an, dass dieses Cmdlet fortgesetzt wird, wenn der Upload eines Vorlagenbilds unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="38d98-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d98-126">CommonParameters</span></span>
<span data-ttu-id="38d98-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d98-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d98-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d98-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38d98-129">INPUTS</span></span>

## <span data-ttu-id="38d98-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38d98-130">OUTPUTS</span></span>

## <span data-ttu-id="38d98-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="38d98-131">NOTES</span></span>

## <span data-ttu-id="38d98-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38d98-132">RELATED LINKS</span></span>

[<span data-ttu-id="38d98-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="38d98-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="38d98-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="38d98-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="38d98-135">Umbenennen – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="38d98-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


