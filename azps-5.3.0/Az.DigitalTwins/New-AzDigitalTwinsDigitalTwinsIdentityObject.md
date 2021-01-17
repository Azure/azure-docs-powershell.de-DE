---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467772"
---
# <span data-ttu-id="80d57-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="80d57-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="80d57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d57-102">SYNOPSIS</span></span>
<span data-ttu-id="80d57-103">Erstellen eines Speicherobjekts für DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="80d57-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="80d57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80d57-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="80d57-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80d57-105">DESCRIPTION</span></span>
<span data-ttu-id="80d57-106">Erstellen eines Speicherobjekts für DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="80d57-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="80d57-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80d57-107">EXAMPLES</span></span>

### <span data-ttu-id="80d57-108">Beispiel 1: Erstellen eines DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="80d57-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="80d57-109">Erstellen eines DigitalTwinsIdentityObject nach ID und Speicherort</span><span class="sxs-lookup"><span data-stu-id="80d57-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="80d57-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80d57-110">PARAMETERS</span></span>

### <span data-ttu-id="80d57-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="80d57-111">-EndpointName</span></span>
<span data-ttu-id="80d57-112">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="80d57-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="80d57-113">-ID</span><span class="sxs-lookup"><span data-stu-id="80d57-113">-Id</span></span>
<span data-ttu-id="80d57-114">Ressourcenidentitätspfad.</span><span class="sxs-lookup"><span data-stu-id="80d57-114">Resource identity path.</span></span>

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

### <span data-ttu-id="80d57-115">-Location</span><span class="sxs-lookup"><span data-stu-id="80d57-115">-Location</span></span>
<span data-ttu-id="80d57-116">Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80d57-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80d57-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d57-117">-ResourceGroupName</span></span>
<span data-ttu-id="80d57-118">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="80d57-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80d57-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="80d57-119">-ResourceName</span></span>
<span data-ttu-id="80d57-120">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="80d57-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80d57-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80d57-121">-SubscriptionId</span></span>
<span data-ttu-id="80d57-122">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="80d57-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="80d57-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d57-123">CommonParameters</span></span>
<span data-ttu-id="80d57-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d57-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d57-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80d57-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d57-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80d57-126">INPUTS</span></span>

## <span data-ttu-id="80d57-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80d57-127">OUTPUTS</span></span>

### <span data-ttu-id="80d57-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="80d57-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="80d57-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80d57-129">NOTES</span></span>

<span data-ttu-id="80d57-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="80d57-130">ALIASES</span></span>

## <span data-ttu-id="80d57-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80d57-131">RELATED LINKS</span></span>

