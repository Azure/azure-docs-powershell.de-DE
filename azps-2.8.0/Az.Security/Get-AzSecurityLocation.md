---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 2de4a80f2770624bb520aa4236a5d92bea97fdf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824856"
---
# <span data-ttu-id="54daa-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="54daa-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="54daa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54daa-102">SYNOPSIS</span></span>
<span data-ttu-id="54daa-103">Ruft den Speicherort ab, an dem Azure Security Center automatisch Daten für das jeweilige Abonnement speichert.</span><span class="sxs-lookup"><span data-stu-id="54daa-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="54daa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54daa-104">SYNTAX</span></span>

### <span data-ttu-id="54daa-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="54daa-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54daa-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="54daa-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54daa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54daa-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54daa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54daa-108">DESCRIPTION</span></span>
<span data-ttu-id="54daa-109">Das Azure Security Center entscheidet automatisch über einen Speicherort, an dem einige Ihrer Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="54daa-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="54daa-110">Verwenden Sie dieses Cmdlet, um diesen Speicherort zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="54daa-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="54daa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54daa-111">EXAMPLES</span></span>

### <span data-ttu-id="54daa-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54daa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="54daa-113">Ruft die Position ab, an der das Azure Security Center die berechneten Sicherheitsdaten speichert.</span><span class="sxs-lookup"><span data-stu-id="54daa-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="54daa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="54daa-114">PARAMETERS</span></span>

### <span data-ttu-id="54daa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54daa-115">-DefaultProfile</span></span>
<span data-ttu-id="54daa-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54daa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54daa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="54daa-117">-Name</span></span>
<span data-ttu-id="54daa-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="54daa-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54daa-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="54daa-119">-ResourceId</span></span>
<span data-ttu-id="54daa-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="54daa-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54daa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54daa-121">CommonParameters</span></span>
<span data-ttu-id="54daa-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54daa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54daa-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54daa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54daa-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54daa-124">INPUTS</span></span>

### <span data-ttu-id="54daa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="54daa-125">System.String</span></span>

## <span data-ttu-id="54daa-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54daa-126">OUTPUTS</span></span>

### <span data-ttu-id="54daa-127">Microsoft. Azure. Commands. Security. Models. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="54daa-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="54daa-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="54daa-128">NOTES</span></span>

## <span data-ttu-id="54daa-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54daa-129">RELATED LINKS</span></span>
