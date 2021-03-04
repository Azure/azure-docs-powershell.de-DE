---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921795"
---
# <span data-ttu-id="49eb5-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="49eb5-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="49eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="49eb5-103">Erstellen Sie ein Office 365-Richtlinienobjekt für Datenverkehrsbruch.</span><span class="sxs-lookup"><span data-stu-id="49eb5-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="49eb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49eb5-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49eb5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="49eb5-106">Erstellen Sie eine Office 365-Breakoutrichtlinie, die mit New-AzVpnSite und Update-AzVpnSite verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="49eb5-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="49eb5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49eb5-107">EXAMPLES</span></span>

### <span data-ttu-id="49eb5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49eb5-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="49eb5-109">Erstellen Sie eine Office 365-Datenverkehrsbruchrichtlinie, bei der breakout zulässig ist, um die Kategorie des Datenverkehrs zu erlauben und zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="49eb5-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="49eb5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49eb5-110">PARAMETERS</span></span>

### <span data-ttu-id="49eb5-111">-Zulassen</span><span class="sxs-lookup"><span data-stu-id="49eb5-111">-Allow</span></span>
<span data-ttu-id="49eb5-112">Durchbrechen des Zulässigen Kategoriedatenverkehrs.</span><span class="sxs-lookup"><span data-stu-id="49eb5-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="49eb5-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="49eb5-113">-Default</span></span>
<span data-ttu-id="49eb5-114">Brechen Sie den standardmäßigen Kategoriedatenverkehr auf.</span><span class="sxs-lookup"><span data-stu-id="49eb5-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="49eb5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49eb5-115">-DefaultProfile</span></span>
<span data-ttu-id="49eb5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49eb5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49eb5-117">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="49eb5-117">-Optimize</span></span>
<span data-ttu-id="49eb5-118">Brechen Sie den Datenverkehr der Kategorie optimieren ab.</span><span class="sxs-lookup"><span data-stu-id="49eb5-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="49eb5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49eb5-119">CommonParameters</span></span>
<span data-ttu-id="49eb5-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49eb5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49eb5-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49eb5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49eb5-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49eb5-122">INPUTS</span></span>

### <span data-ttu-id="49eb5-123">Keine</span><span class="sxs-lookup"><span data-stu-id="49eb5-123">None</span></span>

## <span data-ttu-id="49eb5-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49eb5-124">OUTPUTS</span></span>

### <span data-ttu-id="49eb5-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="49eb5-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="49eb5-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="49eb5-126">NOTES</span></span>

## <span data-ttu-id="49eb5-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="49eb5-127">RELATED LINKS</span></span>
