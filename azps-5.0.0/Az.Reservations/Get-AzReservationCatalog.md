---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302542"
---
# <span data-ttu-id="90bb9-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="90bb9-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="90bb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="90bb9-103">Abrufen des Katalogs verfügbarer Reservierungen</span><span class="sxs-lookup"><span data-stu-id="90bb9-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="90bb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90bb9-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90bb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90bb9-105">DESCRIPTION</span></span>
<span data-ttu-id="90bb9-106">Rufen Sie die Regionen und SKUs ab, die für das angegebene Azure-Abonnement für den Kauf reservierter Instanzen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="90bb9-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="90bb9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90bb9-107">EXAMPLES</span></span>

### <span data-ttu-id="90bb9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90bb9-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="90bb9-109">Abrufen des VirtualMachines-Katalogs in westus für das Standardabonnement</span><span class="sxs-lookup"><span data-stu-id="90bb9-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="90bb9-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="90bb9-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="90bb9-111">Abrufen des SuseLinux-Katalogs für das angegebene Abonnement</span><span class="sxs-lookup"><span data-stu-id="90bb9-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="90bb9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="90bb9-112">PARAMETERS</span></span>

### <span data-ttu-id="90bb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bb9-113">-DefaultProfile</span></span>
<span data-ttu-id="90bb9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90bb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90bb9-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="90bb9-115">-Location</span></span>
<span data-ttu-id="90bb9-116">Gibt den Speicherort der reservierten Ressourcen im Katalog an.</span><span class="sxs-lookup"><span data-stu-id="90bb9-116">Specifies the location of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb9-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="90bb9-117">-ReservedResourceType</span></span>
<span data-ttu-id="90bb9-118">Gibt den Typ der reservierten Ressourcen im Katalog an.</span><span class="sxs-lookup"><span data-stu-id="90bb9-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb9-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="90bb9-119">-SubscriptionId</span></span>
<span data-ttu-id="90bb9-120">ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="90bb9-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bb9-121">CommonParameters</span></span>
<span data-ttu-id="90bb9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90bb9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bb9-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90bb9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bb9-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90bb9-124">INPUTS</span></span>

### <span data-ttu-id="90bb9-125">Keine</span><span class="sxs-lookup"><span data-stu-id="90bb9-125">None</span></span>

## <span data-ttu-id="90bb9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90bb9-126">OUTPUTS</span></span>

### <span data-ttu-id="90bb9-127">Microsoft. Azure. Commands. reservations. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="90bb9-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="90bb9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="90bb9-128">NOTES</span></span>

## <span data-ttu-id="90bb9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90bb9-129">RELATED LINKS</span></span>
