---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 8db3dd9579e528110ec41f59b1c29da5d132d18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502925"
---
# <span data-ttu-id="20f94-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="20f94-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="20f94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20f94-102">SYNOPSIS</span></span>
<span data-ttu-id="20f94-103">Ruft Details zu den vCenter-Servern ab, die für die Ermittlung auf dem vom ASR-Fabric angegebenen Konfigurationsserver registriert sind.</span><span class="sxs-lookup"><span data-stu-id="20f94-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20f94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20f94-104">SYNTAX</span></span>

### <span data-ttu-id="20f94-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="20f94-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20f94-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20f94-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20f94-107">ByName</span><span class="sxs-lookup"><span data-stu-id="20f94-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f94-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20f94-108">DESCRIPTION</span></span>
<span data-ttu-id="20f94-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrvCenter** " ruft Details zu den vCenter-Servern ab, die für die Ermittlung auf dem vom ASR-Fabric angegebenen Konfigurationsserver registriert sind.</span><span class="sxs-lookup"><span data-stu-id="20f94-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="20f94-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20f94-110">EXAMPLES</span></span>

### <span data-ttu-id="20f94-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20f94-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="20f94-112">Holen Sie sich Azure Site Recovery vCenter nach Fabric-Name und Name von vCenter.</span><span class="sxs-lookup"><span data-stu-id="20f94-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="20f94-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20f94-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="20f94-114">Abrufen der Azure-Website-Wiederherstellungs-vCenter-Liste nach Fabric-Namen.</span><span class="sxs-lookup"><span data-stu-id="20f94-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="20f94-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="20f94-115">PARAMETERS</span></span>

### <span data-ttu-id="20f94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f94-116">-DefaultProfile</span></span>
<span data-ttu-id="20f94-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20f94-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f94-118">-Stoff</span><span class="sxs-lookup"><span data-stu-id="20f94-118">-Fabric</span></span>
<span data-ttu-id="20f94-119">ASR-Fabric-Objekt, das den Konfigurations Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="20f94-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20f94-120">-Name</span><span class="sxs-lookup"><span data-stu-id="20f94-120">-Name</span></span>
<span data-ttu-id="20f94-121">Der Name des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="20f94-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f94-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20f94-122">-ResourceId</span></span>
<span data-ttu-id="20f94-123">Gibt die Resourcen-Nr von vCenter an.</span><span class="sxs-lookup"><span data-stu-id="20f94-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f94-124">CommonParameters</span></span>
<span data-ttu-id="20f94-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f94-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f94-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20f94-127">INPUTS</span></span>

### <span data-ttu-id="20f94-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="20f94-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="20f94-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20f94-129">OUTPUTS</span></span>

### <span data-ttu-id="20f94-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="20f94-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="20f94-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="20f94-131">NOTES</span></span>

## <span data-ttu-id="20f94-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20f94-132">RELATED LINKS</span></span>
