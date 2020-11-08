---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006785"
---
# <span data-ttu-id="64218-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="64218-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="64218-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64218-102">SYNOPSIS</span></span>
<span data-ttu-id="64218-103">Ruft Informationen zu Azure RemoteApp-Vorlagen Bildern ab.</span><span class="sxs-lookup"><span data-stu-id="64218-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="64218-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64218-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64218-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64218-105">DESCRIPTION</span></span>
<span data-ttu-id="64218-106">Das Cmdlet " **Get-AzureRemoteAppTemplateImage** " Ruft Informationen zu Azure RemoteApp-Vorlagen Bildern in Microsoft Azure ab.</span><span class="sxs-lookup"><span data-stu-id="64218-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="64218-107">Dieses Cmdlet gibt ein Objekt zurück, das Informationen zu einem angegebenen Vorlagenbild enthält.</span><span class="sxs-lookup"><span data-stu-id="64218-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="64218-108">Wenn kein Vorlagenbild angegeben ist, werden Informationen zu allen Vorlagen Bildern im aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="64218-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="64218-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64218-109">EXAMPLES</span></span>

### <span data-ttu-id="64218-110">Beispiel 1: Abrufen einer Liste aller Vorlagen Bilder</span><span class="sxs-lookup"><span data-stu-id="64218-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="64218-111">Dieser Befehl gibt die Liste aller Vorlagen Bilder zurück.</span><span class="sxs-lookup"><span data-stu-id="64218-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="64218-112">Beispiel 2: Abrufen von Informationen zu einem angegebenen Vorlagenbild</span><span class="sxs-lookup"><span data-stu-id="64218-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="64218-113">Dieser Befehl ruft Informationen zum Vorlagenbild mit dem Namen ContosoApps ab.</span><span class="sxs-lookup"><span data-stu-id="64218-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="64218-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="64218-114">PARAMETERS</span></span>

### <span data-ttu-id="64218-115">-Bildname</span><span class="sxs-lookup"><span data-stu-id="64218-115">-ImageName</span></span>
<span data-ttu-id="64218-116">Gibt den Namen eines Azure RemoteApp-Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="64218-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="64218-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="64218-117">-Profile</span></span>
<span data-ttu-id="64218-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="64218-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64218-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="64218-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64218-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64218-120">CommonParameters</span></span>
<span data-ttu-id="64218-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64218-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64218-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64218-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64218-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64218-123">INPUTS</span></span>

## <span data-ttu-id="64218-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64218-124">OUTPUTS</span></span>

## <span data-ttu-id="64218-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="64218-125">NOTES</span></span>

## <span data-ttu-id="64218-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64218-126">RELATED LINKS</span></span>

[<span data-ttu-id="64218-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="64218-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="64218-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="64218-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


