---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009675"
---
# <span data-ttu-id="6109e-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="6109e-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="6109e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6109e-102">SYNOPSIS</span></span>
<span data-ttu-id="6109e-103">Erstellt eine DNS-Zonenkonfiguration der privaten DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="6109e-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="6109e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6109e-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6109e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6109e-105">DESCRIPTION</span></span>
<span data-ttu-id="6109e-106">Mit dem Cmdlet **New-AzPrivateDnsZoneConfig** können Sie ein neues DNS Zone Configuration-Objekt erstellen, das für die DNS-Zonengruppe eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="6109e-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="6109e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6109e-107">EXAMPLES</span></span>

### <span data-ttu-id="6109e-108">Erstellt eine DNS-Zonenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6109e-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="6109e-109">Im obigen Beispiel wird die DNS-Zone erstellt und dann die DNS-Zonenkonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="6109e-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="6109e-110">`New-AzPrivateDnsZone` das Cmdlet wird vom Modul AZ. PrivateDns geprüft.</span><span class="sxs-lookup"><span data-stu-id="6109e-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="6109e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6109e-111">PARAMETERS</span></span>

### <span data-ttu-id="6109e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6109e-112">-DefaultProfile</span></span>
<span data-ttu-id="6109e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6109e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6109e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6109e-114">-Name</span></span>
<span data-ttu-id="6109e-115">Der Name der Ressource, die innerhalb einer Ressourcengruppe eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="6109e-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="6109e-116">Dieser Name kann für den Zugriff auf die Ressource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6109e-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="6109e-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="6109e-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="6109e-118">Die Ressourcen-ID der privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="6109e-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="6109e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6109e-119">CommonParameters</span></span>
<span data-ttu-id="6109e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6109e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6109e-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6109e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6109e-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6109e-122">INPUTS</span></span>

### <span data-ttu-id="6109e-123">Keine</span><span class="sxs-lookup"><span data-stu-id="6109e-123">None</span></span>

## <span data-ttu-id="6109e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6109e-124">OUTPUTS</span></span>

### <span data-ttu-id="6109e-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="6109e-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="6109e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6109e-126">NOTES</span></span>

## <span data-ttu-id="6109e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6109e-127">RELATED LINKS</span></span>
