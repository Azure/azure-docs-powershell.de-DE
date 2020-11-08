---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006794"
---
# <span data-ttu-id="17d3e-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="17d3e-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="17d3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="17d3e-103">Beendet die angegebene Website.</span><span class="sxs-lookup"><span data-stu-id="17d3e-103">Stops the specified website.</span></span>

## <span data-ttu-id="17d3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d3e-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="17d3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="17d3e-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="17d3e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="17d3e-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="17d3e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="17d3e-108">Das Cmdlet **Stop-AzureWebsite** beendet die angegebene Website, die in Azure gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="17d3e-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="17d3e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17d3e-109">EXAMPLES</span></span>

## <span data-ttu-id="17d3e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d3e-110">PARAMETERS</span></span>

### <span data-ttu-id="17d3e-111">-Name</span><span class="sxs-lookup"><span data-stu-id="17d3e-111">-Name</span></span>
<span data-ttu-id="17d3e-112">Gibt den Namen der Website an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17d3e-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="17d3e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17d3e-113">-PassThru</span></span>
<span data-ttu-id="17d3e-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="17d3e-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="17d3e-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="17d3e-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17d3e-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="17d3e-116">-Profile</span></span>
<span data-ttu-id="17d3e-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="17d3e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17d3e-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="17d3e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17d3e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="17d3e-119">-Slot</span></span>
<span data-ttu-id="17d3e-120">Gibt den Steckplatznamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="17d3e-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="17d3e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d3e-121">CommonParameters</span></span>
<span data-ttu-id="17d3e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17d3e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d3e-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d3e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d3e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17d3e-124">INPUTS</span></span>

## <span data-ttu-id="17d3e-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17d3e-125">OUTPUTS</span></span>

## <span data-ttu-id="17d3e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="17d3e-126">NOTES</span></span>

## <span data-ttu-id="17d3e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17d3e-127">RELATED LINKS</span></span>

[<span data-ttu-id="17d3e-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="17d3e-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="17d3e-129">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="17d3e-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


