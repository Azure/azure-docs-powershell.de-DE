---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005976"
---
# <span data-ttu-id="f8ad6-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f8ad6-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="f8ad6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ad6-103">Startet die angegebene Website.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-103">Starts the specified website.</span></span>

## <span data-ttu-id="f8ad6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ad6-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ad6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ad6-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f8ad6-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f8ad6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f8ad6-108">Das Cmdlet **Start-AzureWebsite** startet eine angegebene Website, die in Azure ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="f8ad6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8ad6-109">EXAMPLES</span></span>

## <span data-ttu-id="f8ad6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="f8ad6-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f8ad6-111">-Name</span></span>
<span data-ttu-id="f8ad6-112">Gibt den Namen der Website an, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="f8ad6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8ad6-113">-PassThru</span></span>
<span data-ttu-id="f8ad6-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8ad6-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8ad6-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="f8ad6-116">-Profile</span></span>
<span data-ttu-id="f8ad6-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f8ad6-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f8ad6-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="f8ad6-119">-Slot</span></span>
<span data-ttu-id="f8ad6-120">Gibt den Steckplatznamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="f8ad6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ad6-121">CommonParameters</span></span>
<span data-ttu-id="f8ad6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ad6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ad6-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ad6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ad6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8ad6-124">INPUTS</span></span>

## <span data-ttu-id="f8ad6-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8ad6-125">OUTPUTS</span></span>

## <span data-ttu-id="f8ad6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8ad6-126">NOTES</span></span>

## <span data-ttu-id="f8ad6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8ad6-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8ad6-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f8ad6-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="f8ad6-129">Neustart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f8ad6-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="f8ad6-130">Satz-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f8ad6-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="f8ad6-131">Anzeigen-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f8ad6-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="f8ad6-132">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f8ad6-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


