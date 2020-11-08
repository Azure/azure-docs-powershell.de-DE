---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005817"
---
# <span data-ttu-id="3a5e0-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="3a5e0-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="3a5e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5e0-103">Ruft verfügbare Planungs Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="3a5e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a5e0-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a5e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a5e0-105">DESCRIPTION</span></span>
<span data-ttu-id="3a5e0-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a5e0-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a5e0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3a5e0-108">Das Cmdlet " **Get-AzureSchedulerLocation** " ruft verfügbare Planungs Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="3a5e0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a5e0-109">EXAMPLES</span></span>

### <span data-ttu-id="3a5e0-110">Beispiel 1: Abrufen verfügbarer Planungs Speicherorte</span><span class="sxs-lookup"><span data-stu-id="3a5e0-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="3a5e0-111">Dieser Befehl ruft verfügbare Planungs Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="3a5e0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a5e0-112">PARAMETERS</span></span>

### <span data-ttu-id="3a5e0-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a5e0-113">-Profile</span></span>
<span data-ttu-id="3a5e0-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a5e0-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a5e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5e0-116">CommonParameters</span></span>
<span data-ttu-id="3a5e0-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5e0-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5e0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5e0-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a5e0-119">INPUTS</span></span>

## <span data-ttu-id="3a5e0-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a5e0-120">OUTPUTS</span></span>

## <span data-ttu-id="3a5e0-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a5e0-121">NOTES</span></span>

## <span data-ttu-id="3a5e0-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a5e0-122">RELATED LINKS</span></span>

[<span data-ttu-id="3a5e0-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="3a5e0-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="3a5e0-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3a5e0-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="3a5e0-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="3a5e0-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


