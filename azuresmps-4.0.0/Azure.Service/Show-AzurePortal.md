---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006154"
---
# <span data-ttu-id="a338c-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="a338c-101">Show-AzurePortal</span></span>

## <span data-ttu-id="a338c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a338c-102">SYNOPSIS</span></span>
<span data-ttu-id="a338c-103">Zeigen Sie das Azure-Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="a338c-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="a338c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a338c-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a338c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a338c-105">DESCRIPTION</span></span>
<span data-ttu-id="a338c-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a338c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a338c-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a338c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a338c-108">Das Cmdlet **Show-AzurePortal** zeigt das Azure-Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="a338c-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="a338c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a338c-109">EXAMPLES</span></span>

### <span data-ttu-id="a338c-110">Beispiel 1: Anzeigen von Informationen zu einer Website</span><span class="sxs-lookup"><span data-stu-id="a338c-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="a338c-111">In diesem Beispiel wird ein Browser im Azure-Portal geöffnet, in dem Informationen zu einer Website mit dem Namen "Meine Website" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a338c-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="a338c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a338c-112">PARAMETERS</span></span>

### <span data-ttu-id="a338c-113">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a338c-113">-Environment</span></span>
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

### <span data-ttu-id="a338c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a338c-114">-Name</span></span>
<span data-ttu-id="a338c-115">Gibt den Namen der Website an, die im Portal angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a338c-115">Specifies the name of the website to show in the portal.</span></span>

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

### <span data-ttu-id="a338c-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="a338c-116">-Profile</span></span>
<span data-ttu-id="a338c-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a338c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a338c-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a338c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a338c-119">-Realm</span><span class="sxs-lookup"><span data-stu-id="a338c-119">-Realm</span></span>
<span data-ttu-id="a338c-120">Gibt die Organisations-ID an, die für die Verbundauthentifizierung verwendet werden soll, wenn das Azure-Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a338c-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

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

### <span data-ttu-id="a338c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a338c-121">CommonParameters</span></span>
<span data-ttu-id="a338c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a338c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a338c-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a338c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a338c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a338c-124">INPUTS</span></span>

## <span data-ttu-id="a338c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a338c-125">OUTPUTS</span></span>

## <span data-ttu-id="a338c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="a338c-126">NOTES</span></span>

## <span data-ttu-id="a338c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a338c-127">RELATED LINKS</span></span>

[<span data-ttu-id="a338c-128">Anzeigen-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a338c-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


