---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006541"
---
# <span data-ttu-id="b7e55-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7e55-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="b7e55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7e55-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e55-103">Ruft die verfügbaren Azure Media Services-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="b7e55-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="b7e55-104">**Hinweis:** Diese Version ist veraltet, bitte lesen Sie die [neuere Version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="b7e55-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b7e55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7e55-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b7e55-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7e55-106">DESCRIPTION</span></span>
<span data-ttu-id="b7e55-107">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b7e55-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b7e55-108">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b7e55-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b7e55-109">Verwenden Sie das Cmdlet, um alle Konten aufzulisten `Get-AzureMediaServicesAccount` .</span><span class="sxs-lookup"><span data-stu-id="b7e55-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="b7e55-110">Verwenden Sie das Cmdlet, um ausführlichere Informationen zu einem bestimmten Konto zu erhalten `Get-AzureMediaServicesAccount -Name YourAccountName` .</span><span class="sxs-lookup"><span data-stu-id="b7e55-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="b7e55-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7e55-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e55-112">Beispiel 1: Auflisten aller Media Services-Konten</span><span class="sxs-lookup"><span data-stu-id="b7e55-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="b7e55-113">Dieser Befehl listet alle verfügbaren Media Services-Konten auf.</span><span class="sxs-lookup"><span data-stu-id="b7e55-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="b7e55-114">Beispiel 2: Abrufen detaillierter Informationen zu einem Media Services-Konto</span><span class="sxs-lookup"><span data-stu-id="b7e55-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="b7e55-115">Mit diesem Befehl werden die Eigenschaften eines Media Services-Kontos angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7e55-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="b7e55-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7e55-116">PARAMETERS</span></span>

### <span data-ttu-id="b7e55-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b7e55-117">-Name</span></span>
<span data-ttu-id="b7e55-118">Der Name des Media Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="b7e55-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="b7e55-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b7e55-119">-Profile</span></span>
<span data-ttu-id="b7e55-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b7e55-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7e55-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b7e55-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7e55-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e55-122">CommonParameters</span></span>
<span data-ttu-id="b7e55-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e55-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e55-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e55-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e55-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7e55-125">INPUTS</span></span>

## <span data-ttu-id="b7e55-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7e55-126">OUTPUTS</span></span>

## <span data-ttu-id="b7e55-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7e55-127">NOTES</span></span>

## <span data-ttu-id="b7e55-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7e55-128">RELATED LINKS</span></span>

[<span data-ttu-id="b7e55-129">Verwenden von Azure PowerShell für Mediendienste</span><span class="sxs-lookup"><span data-stu-id="b7e55-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


