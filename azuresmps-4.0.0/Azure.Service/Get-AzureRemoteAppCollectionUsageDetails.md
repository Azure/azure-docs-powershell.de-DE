---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005838"
---
# <span data-ttu-id="897f1-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="897f1-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="897f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="897f1-102">SYNOPSIS</span></span>
<span data-ttu-id="897f1-103">Ruft Verwendungsdetails für eine Azure RemoteApp-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="897f1-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="897f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="897f1-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="897f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="897f1-105">DESCRIPTION</span></span>
<span data-ttu-id="897f1-106">Das Cmdlet " **Get-AzureRemoteAppCollectionUsageDetails** " ruft Verwendungsdetails für eine Azure RemoteApp-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="897f1-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="897f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="897f1-107">EXAMPLES</span></span>

### <span data-ttu-id="897f1-108">Beispiel 1: Abrufen von Nutzungsdetails für eine Sammlung</span><span class="sxs-lookup"><span data-stu-id="897f1-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="897f1-109">Dieser Befehl ruft Nutzungsdetails für den Monat Dezember im Jahr 2014 für eine Azure RemoteApp-Sammlung mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="897f1-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="897f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="897f1-110">PARAMETERS</span></span>

### <span data-ttu-id="897f1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="897f1-111">-AsJob</span></span>
<span data-ttu-id="897f1-112">Gibt an, dass das Cmdlet als Windows PowerShell-Auftrag im Hintergrund ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="897f1-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

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

### <span data-ttu-id="897f1-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="897f1-113">-CollectionName</span></span>
<span data-ttu-id="897f1-114">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="897f1-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="897f1-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="897f1-115">-Profile</span></span>
<span data-ttu-id="897f1-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="897f1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="897f1-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="897f1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="897f1-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="897f1-118">-UsageMonth</span></span>
<span data-ttu-id="897f1-119">Gibt eine zweistellige Zahl für den Monat an, für den Nutzungsdetails abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="897f1-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="897f1-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="897f1-120">-UsageYear</span></span>
<span data-ttu-id="897f1-121">Gibt das vierstellige Jahr an, für das Verwendungsdetails abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="897f1-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="897f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897f1-122">CommonParameters</span></span>
<span data-ttu-id="897f1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897f1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="897f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897f1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="897f1-125">INPUTS</span></span>

## <span data-ttu-id="897f1-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="897f1-126">OUTPUTS</span></span>

## <span data-ttu-id="897f1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="897f1-127">NOTES</span></span>

## <span data-ttu-id="897f1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="897f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="897f1-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="897f1-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="897f1-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="897f1-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


