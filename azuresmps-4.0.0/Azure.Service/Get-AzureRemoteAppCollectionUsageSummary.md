---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006536"
---
# <span data-ttu-id="392fd-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="392fd-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="392fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="392fd-102">SYNOPSIS</span></span>
<span data-ttu-id="392fd-103">Ruft eine Zusammenfassung der Verwendung für eine Azure RemoteApp-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="392fd-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="392fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="392fd-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="392fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="392fd-105">DESCRIPTION</span></span>
<span data-ttu-id="392fd-106">Das Cmdlet " **Get-AzureRemoteAppCollectionUsageSummary** " Ruft eine Zusammenfassung der Verwendung für eine Azure RemoteApp-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="392fd-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="392fd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="392fd-107">EXAMPLES</span></span>

### <span data-ttu-id="392fd-108">Beispiel 1: Abrufen einer Verwendungszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="392fd-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="392fd-109">Dieser Befehl ruft eine Zusammenfassung der Verwendung für den Monat Dezember im Jahr 2014 für eine Sammlung mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="392fd-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="392fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="392fd-110">PARAMETERS</span></span>

### <span data-ttu-id="392fd-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="392fd-111">-CollectionName</span></span>
<span data-ttu-id="392fd-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="392fd-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="392fd-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="392fd-113">-Profile</span></span>
<span data-ttu-id="392fd-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="392fd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="392fd-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="392fd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="392fd-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="392fd-116">-UsageMonth</span></span>
<span data-ttu-id="392fd-117">Gibt eine zweistellige Zahl für den Monat an, für den eine Verwendungszusammenfassung abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="392fd-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="392fd-118">Wenn dieser Parameter nicht angegeben ist, stellt dieses Cmdlet die Verwendung für den aktuellen Monat bereit.</span><span class="sxs-lookup"><span data-stu-id="392fd-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="392fd-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="392fd-119">-UsageYear</span></span>
<span data-ttu-id="392fd-120">Gibt das vierstellige Jahr an, für das eine Verwendungszusammenfassung abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="392fd-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="392fd-121">Wenn dieser Parameter nicht angegeben ist, wird mit diesem Cmdlet eine Verwendungszusammenfassung für das aktuelle Jahr verwendet.</span><span class="sxs-lookup"><span data-stu-id="392fd-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="392fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392fd-122">CommonParameters</span></span>
<span data-ttu-id="392fd-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="392fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392fd-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="392fd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392fd-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="392fd-125">INPUTS</span></span>

## <span data-ttu-id="392fd-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="392fd-126">OUTPUTS</span></span>

## <span data-ttu-id="392fd-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="392fd-127">NOTES</span></span>

## <span data-ttu-id="392fd-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="392fd-128">RELATED LINKS</span></span>

[<span data-ttu-id="392fd-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="392fd-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="392fd-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="392fd-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


