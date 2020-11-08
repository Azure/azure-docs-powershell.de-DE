---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175024"
---
# <span data-ttu-id="590f9-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="590f9-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="590f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="590f9-102">SYNOPSIS</span></span>
<span data-ttu-id="590f9-103">Erstellen Sie ein Office 365-Datenverkehrs Breakout-Richtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="590f9-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="590f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="590f9-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="590f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="590f9-105">DESCRIPTION</span></span>
<span data-ttu-id="590f9-106">Erstellen Sie eine Office 365-Breakout-Richtlinie, die mit New-AzVpnSite-und Update-AzVpnSite-Cmdlets verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="590f9-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="590f9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="590f9-107">EXAMPLES</span></span>

### <span data-ttu-id="590f9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="590f9-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="590f9-109">Erstellen Sie eine Office 365-Datenverkehrs Breakout-Richtlinie, wobei Breakout für allow und Optimize category of Traffic zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="590f9-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="590f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="590f9-110">PARAMETERS</span></span>

### <span data-ttu-id="590f9-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="590f9-111">-Allow</span></span>
<span data-ttu-id="590f9-112">Ausbruch des Datenverkehrs in der Kategorie "zulassen".</span><span class="sxs-lookup"><span data-stu-id="590f9-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="590f9-113">– Standard</span><span class="sxs-lookup"><span data-stu-id="590f9-113">-Default</span></span>
<span data-ttu-id="590f9-114">Ausbruch des standardmäßigen Kategorie-Datenverkehrs</span><span class="sxs-lookup"><span data-stu-id="590f9-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="590f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590f9-115">-DefaultProfile</span></span>
<span data-ttu-id="590f9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="590f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="590f9-117">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="590f9-117">-Optimize</span></span>
<span data-ttu-id="590f9-118">Ausbruch des Datenverkehrs in der Kategorie optimieren</span><span class="sxs-lookup"><span data-stu-id="590f9-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="590f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590f9-119">CommonParameters</span></span>
<span data-ttu-id="590f9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590f9-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="590f9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590f9-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="590f9-122">INPUTS</span></span>

### <span data-ttu-id="590f9-123">Keine</span><span class="sxs-lookup"><span data-stu-id="590f9-123">None</span></span>

## <span data-ttu-id="590f9-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="590f9-124">OUTPUTS</span></span>

### <span data-ttu-id="590f9-125">Microsoft. Azure. Commands. Network. Models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="590f9-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="590f9-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="590f9-126">NOTES</span></span>

## <span data-ttu-id="590f9-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="590f9-127">RELATED LINKS</span></span>
