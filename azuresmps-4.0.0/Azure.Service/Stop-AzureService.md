---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006013"
---
# <span data-ttu-id="a36ba-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="a36ba-101">Stop-AzureService</span></span>

## <span data-ttu-id="a36ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a36ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a36ba-103">Beendet den aktuellen gehosteten Dienst.</span><span class="sxs-lookup"><span data-stu-id="a36ba-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="a36ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a36ba-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a36ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a36ba-105">DESCRIPTION</span></span>
<span data-ttu-id="a36ba-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a36ba-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a36ba-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a36ba-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a36ba-108">Das Cmdlet **Stop-AzureService** beendet den aktuellen gehosteten Dienst im angegebenen Slot in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="a36ba-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="a36ba-109">Wenn kein Steckplatz angegeben ist, beendet das Cmdlet den Dienst im Produktions Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="a36ba-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="a36ba-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a36ba-110">EXAMPLES</span></span>

## <span data-ttu-id="a36ba-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a36ba-111">PARAMETERS</span></span>

### <span data-ttu-id="a36ba-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a36ba-112">-PassThru</span></span>
<span data-ttu-id="a36ba-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a36ba-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a36ba-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a36ba-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a36ba-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="a36ba-115">-Profile</span></span>
<span data-ttu-id="a36ba-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a36ba-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a36ba-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a36ba-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a36ba-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a36ba-118">-ServiceName</span></span>
<span data-ttu-id="a36ba-119">Gibt den Namen des gehosteten Diensts an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a36ba-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="a36ba-120">Wenn kein Name angegeben wird, beendet das Cmdlet den aktuellen gehosteten Dienst.</span><span class="sxs-lookup"><span data-stu-id="a36ba-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="a36ba-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a36ba-121">-Slot</span></span>
<span data-ttu-id="a36ba-122">Gibt den Steckplatz an, in dem der Dienst gehostet wird, entweder Staging oder Production.</span><span class="sxs-lookup"><span data-stu-id="a36ba-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="a36ba-123">Wenn kein Steckplatz angegeben ist, wird die Produktion angenommen.</span><span class="sxs-lookup"><span data-stu-id="a36ba-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="a36ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36ba-124">CommonParameters</span></span>
<span data-ttu-id="a36ba-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36ba-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a36ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36ba-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a36ba-127">INPUTS</span></span>

## <span data-ttu-id="a36ba-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a36ba-128">OUTPUTS</span></span>

## <span data-ttu-id="a36ba-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a36ba-129">NOTES</span></span>

## <span data-ttu-id="a36ba-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a36ba-130">RELATED LINKS</span></span>

[<span data-ttu-id="a36ba-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="a36ba-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="a36ba-132">Anfang-AzureService</span><span class="sxs-lookup"><span data-stu-id="a36ba-132">Start-AzureService</span></span>](./Start-AzureService.md)


