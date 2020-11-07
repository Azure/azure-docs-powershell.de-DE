---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: aaf0a476601db720674c4422f7e16edfaf0fa2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824039"
---
# <span data-ttu-id="11116-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="11116-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="11116-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11116-102">SYNOPSIS</span></span>
<span data-ttu-id="11116-103">Ruft eine Liste der von Microsoft angebotenen Peering-Service Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="11116-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="11116-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11116-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11116-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11116-105">DESCRIPTION</span></span>
<span data-ttu-id="11116-106">Listen Peering-Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="11116-106">List peering locations.</span></span>

## <span data-ttu-id="11116-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11116-107">EXAMPLES</span></span>

### <span data-ttu-id="11116-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11116-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="11116-109">Ruft die Peering-Speicherorte für Washington ab.</span><span class="sxs-lookup"><span data-stu-id="11116-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="11116-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="11116-110">Example 2</span></span>
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

<span data-ttu-id="11116-111">Ruft die Peering-Speicherorte für Washington ab.</span><span class="sxs-lookup"><span data-stu-id="11116-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="11116-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="11116-112">PARAMETERS</span></span>

### <span data-ttu-id="11116-113">-Land</span><span class="sxs-lookup"><span data-stu-id="11116-113">-Country</span></span>
<span data-ttu-id="11116-114">Der Länder Filter</span><span class="sxs-lookup"><span data-stu-id="11116-114">The country filter</span></span>

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

### <span data-ttu-id="11116-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11116-115">-DefaultProfile</span></span>
<span data-ttu-id="11116-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11116-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11116-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11116-117">CommonParameters</span></span>
<span data-ttu-id="11116-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11116-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11116-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11116-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11116-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11116-120">INPUTS</span></span>

### <span data-ttu-id="11116-121">Keine</span><span class="sxs-lookup"><span data-stu-id="11116-121">None</span></span>

## <span data-ttu-id="11116-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11116-122">OUTPUTS</span></span>

### <span data-ttu-id="11116-123">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="11116-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="11116-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="11116-124">NOTES</span></span>

## <span data-ttu-id="11116-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11116-125">RELATED LINKS</span></span>
