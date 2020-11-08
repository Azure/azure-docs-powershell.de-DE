---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005664"
---
# <span data-ttu-id="4f906-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="4f906-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="4f906-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f906-102">SYNOPSIS</span></span>
<span data-ttu-id="4f906-103">Downloadet und speichert die Protokolle für eine bestimmte Website.</span><span class="sxs-lookup"><span data-stu-id="4f906-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="4f906-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f906-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f906-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f906-105">DESCRIPTION</span></span>
<span data-ttu-id="4f906-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4f906-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4f906-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4f906-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4f906-108">Das Cmdlet **Save-AzureWebsiteLog** downloadet die Protokolle für eine bestimmte Website.</span><span class="sxs-lookup"><span data-stu-id="4f906-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="4f906-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f906-109">EXAMPLES</span></span>

### <span data-ttu-id="4f906-110">Beispiel 1: herunterladen und Speichern von Protokollen für eine Website</span><span class="sxs-lookup"><span data-stu-id="4f906-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="4f906-111">In diesem Beispiel werden die Laufzeit-und Bereitstellungsprotokolle für Website mysite in die Datei logs.zip im aktuellen Verzeichnis heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="4f906-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="4f906-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f906-112">PARAMETERS</span></span>

### <span data-ttu-id="4f906-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4f906-113">-Name</span></span>
<span data-ttu-id="4f906-114">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="4f906-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="4f906-115">-Output</span><span class="sxs-lookup"><span data-stu-id="4f906-115">-Output</span></span>
<span data-ttu-id="4f906-116">Gibt den Pfad zum Speichern der heruntergeladenen Datei an.</span><span class="sxs-lookup"><span data-stu-id="4f906-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="4f906-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f906-117">-PassThru</span></span>
<span data-ttu-id="4f906-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4f906-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f906-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="4f906-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f906-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f906-120">-Profile</span></span>
<span data-ttu-id="4f906-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4f906-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f906-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4f906-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f906-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="4f906-123">-Slot</span></span>
<span data-ttu-id="4f906-124">Gibt den Namen des Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="4f906-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="4f906-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f906-125">CommonParameters</span></span>
<span data-ttu-id="4f906-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f906-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f906-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f906-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f906-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f906-128">INPUTS</span></span>

## <span data-ttu-id="4f906-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f906-129">OUTPUTS</span></span>

## <span data-ttu-id="4f906-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f906-130">NOTES</span></span>

## <span data-ttu-id="4f906-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f906-131">RELATED LINKS</span></span>

[<span data-ttu-id="4f906-132">Wiederherstellen – AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="4f906-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


