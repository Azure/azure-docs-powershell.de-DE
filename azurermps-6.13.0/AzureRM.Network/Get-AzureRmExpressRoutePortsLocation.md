---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664828"
---
# <span data-ttu-id="4ea74-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="4ea74-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="4ea74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ea74-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea74-103">Ruft die Speicherorte ab, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4ea74-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ea74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ea74-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ea74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ea74-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea74-106">Das Cmdlet " **Get-AzureRmExpressRoutePortsLocation** " wird verwendet, um die Speicherorte abzurufen, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4ea74-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="4ea74-107">Bei Angabe einer bestimmten Position als Eingabe zeigt das Cmdlet die Details dieses Speicherorts an, also eine Liste der verfügbaren Bandbreiten an diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="4ea74-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="4ea74-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ea74-108">EXAMPLES</span></span>

### <span data-ttu-id="4ea74-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ea74-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="4ea74-110">Listet die Speicherorte auf, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4ea74-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="4ea74-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ea74-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="4ea74-112">Listet die ExpressRoutePort-Bandbreiten auf, die an Standort $Loc verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4ea74-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="4ea74-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ea74-113">PARAMETERS</span></span>

### <span data-ttu-id="4ea74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea74-114">-DefaultProfile</span></span>
<span data-ttu-id="4ea74-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ea74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea74-116">-Standortname</span><span class="sxs-lookup"><span data-stu-id="4ea74-116">-LocationName</span></span>
<span data-ttu-id="4ea74-117">Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="4ea74-117">The name of the location.</span></span>

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

### <span data-ttu-id="4ea74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea74-118">CommonParameters</span></span>
<span data-ttu-id="4ea74-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea74-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea74-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea74-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ea74-121">INPUTS</span></span>

### <span data-ttu-id="4ea74-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea74-122">System.String</span></span>

## <span data-ttu-id="4ea74-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ea74-123">OUTPUTS</span></span>

### <span data-ttu-id="4ea74-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="4ea74-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="4ea74-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ea74-125">NOTES</span></span>

## <span data-ttu-id="4ea74-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ea74-126">RELATED LINKS</span></span>
