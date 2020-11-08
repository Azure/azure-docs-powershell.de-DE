---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006117"
---
# <span data-ttu-id="948f0-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948f0-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="948f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="948f0-102">SYNOPSIS</span></span>
<span data-ttu-id="948f0-103">Erstellt ein Azure Media Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="948f0-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="948f0-104">**Hinweis:** Diese Version ist veraltet, bitte lesen Sie die [neuere Version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="948f0-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="948f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="948f0-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="948f0-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="948f0-106">DESCRIPTION</span></span>
<span data-ttu-id="948f0-107">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="948f0-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="948f0-108">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="948f0-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="948f0-109">Das Cmdlet **New-AzureMediaServicesAccount** erstellt ein neues Mediendienst Konto mit dem angegebenen Media Services-Kontonamen, dem Datacenter-Speicherort, an dem Sie das Konto erstellen möchten, und einem vorhandenen Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="948f0-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="948f0-110">Das Speicherkonto muss sich im selben Rechenzentrum wie das neue Media Services-Konto befinden.</span><span class="sxs-lookup"><span data-stu-id="948f0-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="948f0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="948f0-111">EXAMPLES</span></span>

### <span data-ttu-id="948f0-112">Beispiel 1: Erstellen eines neuen Media Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="948f0-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="948f0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="948f0-113">PARAMETERS</span></span>

### <span data-ttu-id="948f0-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="948f0-114">-Location</span></span>
<span data-ttu-id="948f0-115">Gibt den Speicherort des Datencenters für Mediendienste an.</span><span class="sxs-lookup"><span data-stu-id="948f0-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="948f0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="948f0-116">-Name</span></span>
<span data-ttu-id="948f0-117">Gibt den Namen des Media Services-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="948f0-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="948f0-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="948f0-118">-Profile</span></span>
<span data-ttu-id="948f0-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="948f0-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="948f0-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="948f0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="948f0-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="948f0-121">-StorageAccountName</span></span>
<span data-ttu-id="948f0-122">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="948f0-122">Specifies the storage account name.</span></span>
<span data-ttu-id="948f0-123">Das Speicherkonto muss bereits im gleichen Rechenzentrum wie das neue Media Services-Konto vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="948f0-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="948f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948f0-124">CommonParameters</span></span>
<span data-ttu-id="948f0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948f0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948f0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="948f0-127">INPUTS</span></span>

## <span data-ttu-id="948f0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="948f0-128">OUTPUTS</span></span>

## <span data-ttu-id="948f0-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="948f0-129">NOTES</span></span>

## <span data-ttu-id="948f0-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="948f0-130">RELATED LINKS</span></span>

[<span data-ttu-id="948f0-131">Verwenden von Azure PowerShell für Mediendienste</span><span class="sxs-lookup"><span data-stu-id="948f0-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="948f0-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948f0-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="948f0-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948f0-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


