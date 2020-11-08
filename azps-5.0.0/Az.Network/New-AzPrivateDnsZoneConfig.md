---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179041"
---
# <span data-ttu-id="cebf1-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="cebf1-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="cebf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cebf1-102">SYNOPSIS</span></span>
<span data-ttu-id="cebf1-103">Erstellt eine DNS-Zonenkonfiguration der privaten DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="cebf1-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="cebf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cebf1-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cebf1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cebf1-105">DESCRIPTION</span></span>
<span data-ttu-id="cebf1-106">Mit dem Cmdlet **New-AzPrivateDnsZoneConfig** können Sie ein neues DNS Zone Configuration-Objekt erstellen, das für die DNS-Zonengruppe eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="cebf1-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="cebf1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cebf1-107">EXAMPLES</span></span>

### <span data-ttu-id="cebf1-108">Erstellt eine DNS-Zonenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cebf1-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="cebf1-109">Im obigen Beispiel wird die DNS-Zone erstellt und dann die DNS-Zonenkonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="cebf1-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="cebf1-110">`New-AzPrivateDnsZone` das Cmdlet wird vom Modul AZ. PrivateDns geprüft.</span><span class="sxs-lookup"><span data-stu-id="cebf1-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="cebf1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cebf1-111">PARAMETERS</span></span>

### <span data-ttu-id="cebf1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebf1-112">-DefaultProfile</span></span>
<span data-ttu-id="cebf1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cebf1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cebf1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cebf1-114">-Name</span></span>
<span data-ttu-id="cebf1-115">Der Name der Ressource, die innerhalb einer Ressourcengruppe eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="cebf1-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="cebf1-116">Dieser Name kann für den Zugriff auf die Ressource verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cebf1-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="cebf1-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="cebf1-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="cebf1-118">Die Ressourcen-ID der privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="cebf1-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="cebf1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebf1-119">CommonParameters</span></span>
<span data-ttu-id="cebf1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebf1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebf1-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cebf1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebf1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cebf1-122">INPUTS</span></span>

### <span data-ttu-id="cebf1-123">Keine</span><span class="sxs-lookup"><span data-stu-id="cebf1-123">None</span></span>

## <span data-ttu-id="cebf1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cebf1-124">OUTPUTS</span></span>

### <span data-ttu-id="cebf1-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="cebf1-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="cebf1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cebf1-126">NOTES</span></span>

## <span data-ttu-id="cebf1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cebf1-127">RELATED LINKS</span></span>
