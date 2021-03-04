---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 77fb1806ba2cbdd2e0398bcdf8289aed62c085fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943702"
---
# <span data-ttu-id="efac8-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="efac8-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="efac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efac8-102">SYNOPSIS</span></span>
<span data-ttu-id="efac8-103">Katalog der verfügbaren Reservierungen herunterladen</span><span class="sxs-lookup"><span data-stu-id="efac8-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="efac8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efac8-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efac8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efac8-105">DESCRIPTION</span></span>
<span data-ttu-id="efac8-106">Hier erhalten Sie die Regionen und Skus, die für den Kauf der reservierten Instanz für das angegebene Azure-Abonnement verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="efac8-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="efac8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efac8-107">EXAMPLES</span></span>

### <span data-ttu-id="efac8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efac8-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="efac8-109">Herunterladen des VirtualMachines-Katalogs in westus für das Standardabonnement</span><span class="sxs-lookup"><span data-stu-id="efac8-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="efac8-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="efac8-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="efac8-111">Herunterladen des SuseLinux-Katalogs für das angegebene Abonnement</span><span class="sxs-lookup"><span data-stu-id="efac8-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="efac8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="efac8-112">PARAMETERS</span></span>

### <span data-ttu-id="efac8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efac8-113">-DefaultProfile</span></span>
<span data-ttu-id="efac8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efac8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efac8-115">-Location</span><span class="sxs-lookup"><span data-stu-id="efac8-115">-Location</span></span>
<span data-ttu-id="efac8-116">Gibt den Speicherort der reservierten Ressourcen im Katalog an.</span><span class="sxs-lookup"><span data-stu-id="efac8-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="efac8-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="efac8-117">-ReservedResourceType</span></span>
<span data-ttu-id="efac8-118">Gibt den Typ der reservierten Ressourcen im Katalog an.</span><span class="sxs-lookup"><span data-stu-id="efac8-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="efac8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efac8-119">-SubscriptionId</span></span>
<span data-ttu-id="efac8-120">ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="efac8-120">Id of the subscription</span></span>

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

### <span data-ttu-id="efac8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efac8-121">CommonParameters</span></span>
<span data-ttu-id="efac8-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efac8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efac8-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efac8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efac8-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efac8-124">INPUTS</span></span>

### <span data-ttu-id="efac8-125">Keine</span><span class="sxs-lookup"><span data-stu-id="efac8-125">None</span></span>

## <span data-ttu-id="efac8-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efac8-126">OUTPUTS</span></span>

### <span data-ttu-id="efac8-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="efac8-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="efac8-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="efac8-128">NOTES</span></span>

## <span data-ttu-id="efac8-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="efac8-129">RELATED LINKS</span></span>
