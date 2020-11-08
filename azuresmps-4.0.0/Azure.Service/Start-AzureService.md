---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006236"
---
# <span data-ttu-id="0c163-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="0c163-101">Start-AzureService</span></span>

## <span data-ttu-id="0c163-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c163-102">SYNOPSIS</span></span>
<span data-ttu-id="0c163-103">Startet den angegebenen gehosteten Dienst in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="0c163-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="0c163-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c163-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c163-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c163-105">DESCRIPTION</span></span>
<span data-ttu-id="0c163-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c163-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0c163-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0c163-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0c163-108">Das Cmdlet **Start-AzureService** startet den angegebenen gehosteten Dienst in Windows Azure, wenn sich der Dienst im Zustand Stopped befindet.</span><span class="sxs-lookup"><span data-stu-id="0c163-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="0c163-109">Beachten Sie, dass das Cmdlet **Publish-AzureServiceProject** automatisch versucht, den Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="0c163-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="0c163-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c163-110">EXAMPLES</span></span>

## <span data-ttu-id="0c163-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c163-111">PARAMETERS</span></span>

### <span data-ttu-id="0c163-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c163-112">-PassThru</span></span>
<span data-ttu-id="0c163-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0c163-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0c163-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0c163-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c163-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="0c163-115">-Profile</span></span>
<span data-ttu-id="0c163-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0c163-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c163-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0c163-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c163-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c163-118">-ServiceName</span></span>
<span data-ttu-id="0c163-119">Gibt den Namen des gehosteten Diensts an, der gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c163-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="0c163-120">Wenn kein Name angegeben ist, startet das Cmdlet den aktuellen gehosteten Dienst.</span><span class="sxs-lookup"><span data-stu-id="0c163-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="0c163-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="0c163-121">-Slot</span></span>
<span data-ttu-id="0c163-122">Gibt den Bereitstellungs Steckplatz an, in dem der Dienst gestartet werden soll, entweder Staging oder Production.</span><span class="sxs-lookup"><span data-stu-id="0c163-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="0c163-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c163-123">CommonParameters</span></span>
<span data-ttu-id="0c163-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c163-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c163-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c163-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c163-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c163-126">INPUTS</span></span>

## <span data-ttu-id="0c163-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c163-127">OUTPUTS</span></span>

## <span data-ttu-id="0c163-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c163-128">NOTES</span></span>

## <span data-ttu-id="0c163-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c163-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c163-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="0c163-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="0c163-131">Anfang-AzureService</span><span class="sxs-lookup"><span data-stu-id="0c163-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="0c163-132">Stopp-AzureService</span><span class="sxs-lookup"><span data-stu-id="0c163-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


