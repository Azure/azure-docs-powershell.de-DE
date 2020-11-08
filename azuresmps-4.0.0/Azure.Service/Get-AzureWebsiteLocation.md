---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006478"
---
# <span data-ttu-id="d21f9-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="d21f9-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="d21f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d21f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d21f9-103">Ruft alle verfügbaren Websitespeicher Orte ab.</span><span class="sxs-lookup"><span data-stu-id="d21f9-103">Gets all available website locations.</span></span>

## <span data-ttu-id="d21f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d21f9-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d21f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d21f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d21f9-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d21f9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d21f9-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d21f9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d21f9-108">Ruft alle verfügbaren Websitespeicher Orte für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d21f9-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="d21f9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d21f9-109">EXAMPLES</span></span>

### <span data-ttu-id="d21f9-110">Beispiel 1: Abrufen aller verfügbaren Speicherorte</span><span class="sxs-lookup"><span data-stu-id="d21f9-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="d21f9-111">In diesem Beispiel werden alle verfügbaren Websitespeicher Orte für das aktuelle Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d21f9-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="d21f9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d21f9-112">PARAMETERS</span></span>

### <span data-ttu-id="d21f9-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="d21f9-113">-Profile</span></span>
<span data-ttu-id="d21f9-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d21f9-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d21f9-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d21f9-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d21f9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21f9-116">CommonParameters</span></span>
<span data-ttu-id="d21f9-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d21f9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21f9-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d21f9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21f9-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d21f9-119">INPUTS</span></span>

## <span data-ttu-id="d21f9-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d21f9-120">OUTPUTS</span></span>

## <span data-ttu-id="d21f9-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="d21f9-121">NOTES</span></span>

## <span data-ttu-id="d21f9-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d21f9-122">RELATED LINKS</span></span>

[<span data-ttu-id="d21f9-123">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d21f9-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


