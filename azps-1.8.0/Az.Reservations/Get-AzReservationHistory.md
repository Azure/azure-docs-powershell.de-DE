---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cf68c40a13247d1101f6d25abac92f01ae1a0053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659687"
---
# <span data-ttu-id="67082-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="67082-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="67082-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67082-102">SYNOPSIS</span></span>
<span data-ttu-id="67082-103">Abrufen des `Reservation` Versionsverlaufs</span><span class="sxs-lookup"><span data-stu-id="67082-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="67082-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67082-104">SYNTAX</span></span>

### <span data-ttu-id="67082-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="67082-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67082-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="67082-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67082-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67082-107">DESCRIPTION</span></span>
<span data-ttu-id="67082-108">Liste aller Überarbeitungen für die `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="67082-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="67082-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67082-109">EXAMPLES</span></span>

### <span data-ttu-id="67082-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67082-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="67082-111">Abrufen des Versionsverlaufs der jeweiligen Reservierung</span><span class="sxs-lookup"><span data-stu-id="67082-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="67082-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="67082-112">PARAMETERS</span></span>

### <span data-ttu-id="67082-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67082-113">-DefaultProfile</span></span>
<span data-ttu-id="67082-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67082-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67082-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="67082-115">-Reservation</span></span>
<span data-ttu-id="67082-116">Pipe-Objektparameter für `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="67082-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="67082-117">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="67082-117">-ReservationId</span></span>
<span data-ttu-id="67082-118">Reservierungs-Nr. des `Reservation` Verlaufs, der angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="67082-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="67082-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="67082-119">-ReservationOrderId</span></span>
<span data-ttu-id="67082-120">ReservationOrderId für das `ReservationOrder` , das die `Reservation`</span><span class="sxs-lookup"><span data-stu-id="67082-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="67082-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67082-121">CommonParameters</span></span>
<span data-ttu-id="67082-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67082-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67082-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67082-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67082-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67082-124">INPUTS</span></span>

### <span data-ttu-id="67082-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="67082-125">System.Guid</span></span>

### <span data-ttu-id="67082-126">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="67082-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="67082-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67082-127">OUTPUTS</span></span>

### <span data-ttu-id="67082-128">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="67082-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="67082-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="67082-129">NOTES</span></span>

## <span data-ttu-id="67082-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67082-130">RELATED LINKS</span></span>
