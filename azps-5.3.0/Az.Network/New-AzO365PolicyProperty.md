---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467328"
---
# <span data-ttu-id="89d1b-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="89d1b-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="89d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="89d1b-103">Erstellen Sie ein Office 365-Richtlinienobjekt für die Unterbrechung des Datenverkehrs.</span><span class="sxs-lookup"><span data-stu-id="89d1b-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="89d1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89d1b-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89d1b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="89d1b-106">Erstellen Sie eine Office 365-Breakoutrichtlinie für die Verwendung mit New-AzVpnSite und Update-AzVpnSite Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="89d1b-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="89d1b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="89d1b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89d1b-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="89d1b-109">Erstellen Sie eine Office 365-Richtlinie für Verkehrsbehinderungen mit einer zulässigen Unterbrechung für die Zulassen und Optimierung der Kategorie von Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="89d1b-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="89d1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89d1b-110">PARAMETERS</span></span>

### <span data-ttu-id="89d1b-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="89d1b-111">-Allow</span></span>
<span data-ttu-id="89d1b-112">Unterbrechen Sie den zulässigen Kategoriedatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="89d1b-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d1b-113">-Default</span><span class="sxs-lookup"><span data-stu-id="89d1b-113">-Default</span></span>
<span data-ttu-id="89d1b-114">Verdingen Sie den Standardmäßigen Kategoriedatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="89d1b-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d1b-115">-DefaultProfile</span></span>
<span data-ttu-id="89d1b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89d1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d1b-117">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="89d1b-117">-Optimize</span></span>
<span data-ttu-id="89d1b-118">Unterbrechen Sie den Optimierungskategoriedatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="89d1b-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d1b-119">CommonParameters</span></span>
<span data-ttu-id="89d1b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d1b-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89d1b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d1b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89d1b-122">INPUTS</span></span>

### <span data-ttu-id="89d1b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="89d1b-123">None</span></span>

## <span data-ttu-id="89d1b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89d1b-124">OUTPUTS</span></span>

### <span data-ttu-id="89d1b-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="89d1b-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="89d1b-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89d1b-126">NOTES</span></span>

## <span data-ttu-id="89d1b-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89d1b-127">RELATED LINKS</span></span>
