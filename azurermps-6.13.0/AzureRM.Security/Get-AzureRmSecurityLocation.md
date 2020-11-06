---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477694"
---
# <span data-ttu-id="5f78d-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="5f78d-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="5f78d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f78d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f78d-103">Ruft den Speicherort ab, an dem Azure Security Center automatisch Daten für das jeweilige Abonnement speichert.</span><span class="sxs-lookup"><span data-stu-id="5f78d-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f78d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f78d-104">SYNTAX</span></span>

### <span data-ttu-id="5f78d-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f78d-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f78d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5f78d-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f78d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f78d-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f78d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f78d-108">DESCRIPTION</span></span>
<span data-ttu-id="5f78d-109">Das Azure Security Center entscheidet automatisch über einen Speicherort, an dem einige Ihrer Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5f78d-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="5f78d-110">Verwenden Sie dieses Cmdlet, um diesen Speicherort zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5f78d-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="5f78d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f78d-111">EXAMPLES</span></span>

### <span data-ttu-id="5f78d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f78d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="5f78d-113">Ruft die Position ab, an der das Azure Security Center die berechneten Sicherheitsdaten speichert.</span><span class="sxs-lookup"><span data-stu-id="5f78d-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="5f78d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f78d-114">PARAMETERS</span></span>

### <span data-ttu-id="5f78d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f78d-115">-DefaultProfile</span></span>
<span data-ttu-id="5f78d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f78d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f78d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5f78d-117">-Name</span></span>
<span data-ttu-id="5f78d-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="5f78d-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f78d-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f78d-119">-ResourceId</span></span>
<span data-ttu-id="5f78d-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5f78d-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f78d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f78d-121">CommonParameters</span></span>
<span data-ttu-id="5f78d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f78d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f78d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f78d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f78d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f78d-124">INPUTS</span></span>

### <span data-ttu-id="5f78d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5f78d-125">System.String</span></span>

## <span data-ttu-id="5f78d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f78d-126">OUTPUTS</span></span>

### <span data-ttu-id="5f78d-127">Microsoft. Azure. Commands. Security. Models. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="5f78d-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="5f78d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f78d-128">NOTES</span></span>

## <span data-ttu-id="5f78d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f78d-129">RELATED LINKS</span></span>
