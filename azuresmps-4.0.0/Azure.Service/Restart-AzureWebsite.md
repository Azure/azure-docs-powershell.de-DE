---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005676"
---
# <span data-ttu-id="b1b68-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b1b68-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="b1b68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1b68-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b68-103">Beendet die angegebene Website und startet Sie neu.</span><span class="sxs-lookup"><span data-stu-id="b1b68-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="b1b68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b68-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1b68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1b68-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b68-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b1b68-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b1b68-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b1b68-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b1b68-108">Mit dem Cmdlet " **Restart-AzureWebsite** " wird die angegebene Website beendet und neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="b1b68-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="b1b68-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1b68-109">EXAMPLES</span></span>

### <span data-ttu-id="b1b68-110">Beispiel 1: Erneutes Starten einer Website</span><span class="sxs-lookup"><span data-stu-id="b1b68-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="b1b68-111">In diesem Beispiel wird eine Website mit dem Namen "mywebsite" neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="b1b68-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="b1b68-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b68-112">PARAMETERS</span></span>

### <span data-ttu-id="b1b68-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b1b68-113">-Name</span></span>
<span data-ttu-id="b1b68-114">Gibt den Namen der Azure-Website an, die neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1b68-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="b1b68-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1b68-115">-PassThru</span></span>
<span data-ttu-id="b1b68-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b1b68-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1b68-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b1b68-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1b68-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1b68-118">-Profile</span></span>
<span data-ttu-id="b1b68-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b1b68-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1b68-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b1b68-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1b68-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="b1b68-121">-Slot</span></span>
<span data-ttu-id="b1b68-122">Gibt den Steckplatznamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="b1b68-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="b1b68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b68-123">CommonParameters</span></span>
<span data-ttu-id="b1b68-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b68-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b68-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b68-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1b68-126">INPUTS</span></span>

## <span data-ttu-id="b1b68-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1b68-127">OUTPUTS</span></span>

## <span data-ttu-id="b1b68-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1b68-128">NOTES</span></span>

## <span data-ttu-id="b1b68-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1b68-129">RELATED LINKS</span></span>

[<span data-ttu-id="b1b68-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b1b68-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="b1b68-131">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b1b68-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b1b68-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b1b68-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="b1b68-133">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b1b68-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


