---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 84cc6f2e8e51de6176b4ab8a04296aab8516a967
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937720"
---
# <span data-ttu-id="eee75-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="eee75-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="eee75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee75-102">SYNOPSIS</span></span>
<span data-ttu-id="eee75-103">Ruft eine Liste der von Microsoft angebotenen Peeringdienststandorte ab.</span><span class="sxs-lookup"><span data-stu-id="eee75-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="eee75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eee75-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eee75-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee75-105">DESCRIPTION</span></span>
<span data-ttu-id="eee75-106">Listen peering-Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="eee75-106">List peering locations.</span></span>

## <span data-ttu-id="eee75-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eee75-107">EXAMPLES</span></span>

### <span data-ttu-id="eee75-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eee75-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="eee75-109">Ruft die Peeringstandorte für washington ab.</span><span class="sxs-lookup"><span data-stu-id="eee75-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="eee75-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eee75-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="eee75-111">Ruft die Peeringstandorte für washington ab.</span><span class="sxs-lookup"><span data-stu-id="eee75-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="eee75-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eee75-112">PARAMETERS</span></span>

### <span data-ttu-id="eee75-113">-Land</span><span class="sxs-lookup"><span data-stu-id="eee75-113">-Country</span></span>
<span data-ttu-id="eee75-114">Der Länderfilter</span><span class="sxs-lookup"><span data-stu-id="eee75-114">The country filter</span></span>

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

### <span data-ttu-id="eee75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee75-115">-DefaultProfile</span></span>
<span data-ttu-id="eee75-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eee75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eee75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee75-117">CommonParameters</span></span>
<span data-ttu-id="eee75-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee75-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eee75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee75-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eee75-120">INPUTS</span></span>

### <span data-ttu-id="eee75-121">Keine</span><span class="sxs-lookup"><span data-stu-id="eee75-121">None</span></span>

## <span data-ttu-id="eee75-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eee75-122">OUTPUTS</span></span>

### <span data-ttu-id="eee75-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="eee75-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="eee75-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eee75-124">NOTES</span></span>

## <span data-ttu-id="eee75-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eee75-125">RELATED LINKS</span></span>
