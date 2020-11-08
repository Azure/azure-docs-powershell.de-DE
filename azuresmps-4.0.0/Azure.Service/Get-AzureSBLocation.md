---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006518"
---
# <span data-ttu-id="3a048-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="3a048-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="3a048-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a048-102">SYNOPSIS</span></span>
<span data-ttu-id="3a048-103">Ruft den Standort des ServiceBus ab.</span><span class="sxs-lookup"><span data-stu-id="3a048-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="3a048-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a048-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a048-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a048-105">DESCRIPTION</span></span>
<span data-ttu-id="3a048-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a048-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a048-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a048-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3a048-108">Das Cmdlet " **Get-AzureSBLocation** " gibt die Speicherorte zurück, von denen der ServiceBus verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3a048-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="3a048-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a048-109">EXAMPLES</span></span>

### <span data-ttu-id="3a048-110">Beispiel 1: Abrufen des ServiceBus-Standorts</span><span class="sxs-lookup"><span data-stu-id="3a048-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="3a048-111">In diesem Beispiel wird der Standort des ServiceBus abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a048-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="3a048-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a048-112">PARAMETERS</span></span>

### <span data-ttu-id="3a048-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a048-113">-Profile</span></span>
<span data-ttu-id="3a048-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3a048-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a048-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3a048-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a048-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a048-116">CommonParameters</span></span>
<span data-ttu-id="3a048-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a048-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a048-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a048-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a048-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a048-119">INPUTS</span></span>

## <span data-ttu-id="3a048-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a048-120">OUTPUTS</span></span>

## <span data-ttu-id="3a048-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a048-121">NOTES</span></span>

## <span data-ttu-id="3a048-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a048-122">RELATED LINKS</span></span>

[<span data-ttu-id="3a048-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="3a048-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


