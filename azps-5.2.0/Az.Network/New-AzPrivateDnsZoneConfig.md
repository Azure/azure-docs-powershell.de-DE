---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368134"
---
# <span data-ttu-id="f7f21-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="f7f21-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="f7f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f21-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f21-103">Erstellt die KONFIGURATION der DNS-Zone der Gruppe der privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="f7f21-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="f7f21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7f21-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7f21-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7f21-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f21-106">Mit **dem Cmdlet "New-AzPrivateDnsZoneConfig"** können Sie ein neues Konfigurationsobjekt für die DNS-Zone erstellen, das für die Gruppe "DNS-Zone" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f21-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="f7f21-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7f21-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f21-108">Erstellt eine Konfiguration der DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="f7f21-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="f7f21-109">Im vorstehenden Beispiel wird die DNS-Zone und dann die Konfiguration der DNS-Zone erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7f21-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="f7f21-110">`New-AzPrivateDnsZone` Das Cmdlet Az.PrivateDns zeigt den Beweis für das Modul Az.PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="f7f21-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="f7f21-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7f21-111">PARAMETERS</span></span>

### <span data-ttu-id="f7f21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f21-112">-DefaultProfile</span></span>
<span data-ttu-id="f7f21-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7f21-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f21-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f21-114">-Name</span></span>
<span data-ttu-id="f7f21-115">Der Name der Ressource, die innerhalb einer Ressourcengruppe eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="f7f21-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="f7f21-116">Dieser Name kann für den Zugriff auf die Ressource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7f21-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f21-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="f7f21-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="f7f21-118">Die Ressourcen-ID der privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="f7f21-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="f7f21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f21-119">CommonParameters</span></span>
<span data-ttu-id="f7f21-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f21-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7f21-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f21-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7f21-122">INPUTS</span></span>

### <span data-ttu-id="f7f21-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f7f21-123">None</span></span>

## <span data-ttu-id="f7f21-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7f21-124">OUTPUTS</span></span>

### <span data-ttu-id="f7f21-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="f7f21-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="f7f21-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7f21-126">NOTES</span></span>

## <span data-ttu-id="f7f21-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7f21-127">RELATED LINKS</span></span>
