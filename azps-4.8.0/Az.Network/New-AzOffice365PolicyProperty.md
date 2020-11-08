---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 82ff7d915a7ddc2d15655513dade28fc1e7ffff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175022"
---
# <span data-ttu-id="116ac-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="116ac-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="116ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="116ac-102">SYNOPSIS</span></span>
<span data-ttu-id="116ac-103">Definieren einer neuen Office 365-Datenverkehrs-Breakout-Richtlinie für die Verwendung mit einer virtuellen Appliance-Website.</span><span class="sxs-lookup"><span data-stu-id="116ac-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="116ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="116ac-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="116ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="116ac-105">DESCRIPTION</span></span>
<span data-ttu-id="116ac-106">Der Befehl New-AzOffice365PolicyProperties definiert eine Office 365-Breakout-Richtlinie, die woith einer virtuellen Appliance-Website verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="116ac-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used woith a Virtual Appliance site.</span></span> 

## <span data-ttu-id="116ac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="116ac-107">EXAMPLES</span></span>

### <span data-ttu-id="116ac-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="116ac-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="116ac-109">Erstellen Sie das Office 365 Traffic-Breakout-Richtlinienobjekt, das mit Virtual Appliance-Website Befehlen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="116ac-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="116ac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="116ac-110">PARAMETERS</span></span>

### <span data-ttu-id="116ac-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="116ac-111">-Allow</span></span>
<span data-ttu-id="116ac-112">Ausbruch des Datenverkehrs in der Kategorie "zulassen".</span><span class="sxs-lookup"><span data-stu-id="116ac-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="116ac-113">– Standard</span><span class="sxs-lookup"><span data-stu-id="116ac-113">-Default</span></span>
<span data-ttu-id="116ac-114">Ausbruch des standardmäßigen Kategorie-Datenverkehrs</span><span class="sxs-lookup"><span data-stu-id="116ac-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="116ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116ac-115">-DefaultProfile</span></span>
<span data-ttu-id="116ac-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="116ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116ac-117">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="116ac-117">-Optimize</span></span>
<span data-ttu-id="116ac-118">Ausbruch des Datenverkehrs in der Kategorie optimieren</span><span class="sxs-lookup"><span data-stu-id="116ac-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="116ac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116ac-119">CommonParameters</span></span>
<span data-ttu-id="116ac-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116ac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116ac-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="116ac-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116ac-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="116ac-122">INPUTS</span></span>

### <span data-ttu-id="116ac-123">Keine</span><span class="sxs-lookup"><span data-stu-id="116ac-123">None</span></span>

## <span data-ttu-id="116ac-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="116ac-124">OUTPUTS</span></span>

### <span data-ttu-id="116ac-125">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="116ac-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="116ac-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="116ac-126">NOTES</span></span>

## <span data-ttu-id="116ac-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="116ac-127">RELATED LINKS</span></span>
