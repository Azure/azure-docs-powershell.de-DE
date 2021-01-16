---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295337"
---
# <span data-ttu-id="8b242-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="8b242-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="8b242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b242-102">SYNOPSIS</span></span>
<span data-ttu-id="8b242-103">Ruft den Speicherort ab, an dem Azure Security Center automatisch Daten für das spezifische Abonnement gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8b242-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="8b242-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b242-104">SYNTAX</span></span>

### <span data-ttu-id="8b242-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b242-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b242-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8b242-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b242-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b242-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b242-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b242-108">DESCRIPTION</span></span>
<span data-ttu-id="8b242-109">Azure Security Center entscheidet automatisch über einen Speicherort für einige Ihrer Daten.</span><span class="sxs-lookup"><span data-stu-id="8b242-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="8b242-110">Verwenden Sie dieses Cmdlet, um diesen Speicherort zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8b242-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="8b242-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b242-111">EXAMPLES</span></span>

### <span data-ttu-id="8b242-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b242-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="8b242-113">Ruft den Speicherort ab, an dem das Azure Security Center die berechneten Sicherheitsdaten speichert.</span><span class="sxs-lookup"><span data-stu-id="8b242-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="8b242-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b242-114">PARAMETERS</span></span>

### <span data-ttu-id="8b242-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b242-115">-DefaultProfile</span></span>
<span data-ttu-id="8b242-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b242-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b242-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8b242-117">-Name</span></span>
<span data-ttu-id="8b242-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8b242-118">Resource name.</span></span>

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

### <span data-ttu-id="8b242-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b242-119">-ResourceId</span></span>
<span data-ttu-id="8b242-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8b242-120">Resource ID.</span></span>

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

### <span data-ttu-id="8b242-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b242-121">CommonParameters</span></span>
<span data-ttu-id="8b242-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b242-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b242-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b242-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b242-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b242-124">INPUTS</span></span>

### <span data-ttu-id="8b242-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8b242-125">System.String</span></span>

## <span data-ttu-id="8b242-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b242-126">OUTPUTS</span></span>

### <span data-ttu-id="8b242-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="8b242-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="8b242-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b242-128">NOTES</span></span>

## <span data-ttu-id="8b242-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b242-129">RELATED LINKS</span></span>
