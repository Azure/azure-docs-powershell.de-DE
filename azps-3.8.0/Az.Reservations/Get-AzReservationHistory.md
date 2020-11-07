---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846820"
---
# <span data-ttu-id="95c38-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="95c38-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="95c38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95c38-102">SYNOPSIS</span></span>
<span data-ttu-id="95c38-103">Abrufen des `Reservation` Versionsverlaufs</span><span class="sxs-lookup"><span data-stu-id="95c38-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="95c38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95c38-104">SYNTAX</span></span>

### <span data-ttu-id="95c38-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="95c38-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95c38-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="95c38-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95c38-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95c38-107">DESCRIPTION</span></span>
<span data-ttu-id="95c38-108">Liste aller Überarbeitungen für die `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="95c38-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="95c38-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95c38-109">EXAMPLES</span></span>

### <span data-ttu-id="95c38-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95c38-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="95c38-111">Abrufen des Versionsverlaufs der jeweiligen Reservierung</span><span class="sxs-lookup"><span data-stu-id="95c38-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="95c38-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="95c38-112">PARAMETERS</span></span>

### <span data-ttu-id="95c38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c38-113">-DefaultProfile</span></span>
<span data-ttu-id="95c38-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95c38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c38-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="95c38-115">-Reservation</span></span>
<span data-ttu-id="95c38-116">Pipe-Objektparameter für `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="95c38-116">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95c38-117">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="95c38-117">-ReservationId</span></span>
<span data-ttu-id="95c38-118">Reservierungs-Nr. des `Reservation` Verlaufs, der angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="95c38-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c38-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="95c38-119">-ReservationOrderId</span></span>
<span data-ttu-id="95c38-120">ReservationOrderId für das `ReservationOrder` , das die `Reservation`</span><span class="sxs-lookup"><span data-stu-id="95c38-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c38-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c38-121">CommonParameters</span></span>
<span data-ttu-id="95c38-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c38-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c38-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95c38-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c38-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95c38-124">INPUTS</span></span>

### <span data-ttu-id="95c38-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="95c38-125">System.Guid</span></span>

### <span data-ttu-id="95c38-126">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="95c38-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="95c38-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95c38-127">OUTPUTS</span></span>

### <span data-ttu-id="95c38-128">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="95c38-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="95c38-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="95c38-129">NOTES</span></span>

## <span data-ttu-id="95c38-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95c38-130">RELATED LINKS</span></span>
