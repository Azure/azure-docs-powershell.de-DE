---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005680"
---
# <span data-ttu-id="0710c-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="0710c-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="0710c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0710c-102">SYNOPSIS</span></span>
<span data-ttu-id="0710c-103">Benennt ein Azure RemoteApp-Vorlagenbild um.</span><span class="sxs-lookup"><span data-stu-id="0710c-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="0710c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0710c-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0710c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0710c-105">DESCRIPTION</span></span>
<span data-ttu-id="0710c-106">Mit dem Cmdlet **Rename-AzureRemoteAppTemplateImage** wird ein Azure RemoteApp-Vorlagenbild umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0710c-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="0710c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0710c-107">EXAMPLES</span></span>

### <span data-ttu-id="0710c-108">Beispiel 1: Umbenennen eines Vorlagenbilds</span><span class="sxs-lookup"><span data-stu-id="0710c-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="0710c-109">Mit diesem Befehl wird das Azure RemoteApp-Vorlagenbild mit dem Namen ContosoApps in ContosoFinanceApps umbenannt.</span><span class="sxs-lookup"><span data-stu-id="0710c-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="0710c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0710c-110">PARAMETERS</span></span>

### <span data-ttu-id="0710c-111">-Bildname</span><span class="sxs-lookup"><span data-stu-id="0710c-111">-ImageName</span></span>
<span data-ttu-id="0710c-112">Gibt den Namen eines Azure RemoteApp-Vorlagenbilds an, das umbenannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0710c-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

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

### <span data-ttu-id="0710c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0710c-113">-NewName</span></span>
<span data-ttu-id="0710c-114">Gibt einen neuen Namen für ein Azure RemoteApp-Vorlagenbild an.</span><span class="sxs-lookup"><span data-stu-id="0710c-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="0710c-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="0710c-115">-Profile</span></span>
<span data-ttu-id="0710c-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0710c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0710c-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0710c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0710c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0710c-118">CommonParameters</span></span>
<span data-ttu-id="0710c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0710c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0710c-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0710c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0710c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0710c-121">INPUTS</span></span>

## <span data-ttu-id="0710c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0710c-122">OUTPUTS</span></span>

## <span data-ttu-id="0710c-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="0710c-123">NOTES</span></span>

## <span data-ttu-id="0710c-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0710c-124">RELATED LINKS</span></span>

[<span data-ttu-id="0710c-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="0710c-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="0710c-126">Neu – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="0710c-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="0710c-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="0710c-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


