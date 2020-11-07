---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 48437526fdaf8ae226ff7693b417fcff7ffc93d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824368"
---
# <span data-ttu-id="7bec0-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="7bec0-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="7bec0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bec0-102">SYNOPSIS</span></span>
<span data-ttu-id="7bec0-103">Ruft Details zu den vCenter-Servern ab, die für die Ermittlung auf dem vom ASR-Fabric angegebenen Konfigurationsserver registriert sind.</span><span class="sxs-lookup"><span data-stu-id="7bec0-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="7bec0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bec0-104">SYNTAX</span></span>

### <span data-ttu-id="7bec0-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bec0-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bec0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bec0-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bec0-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7bec0-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bec0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bec0-108">DESCRIPTION</span></span>
<span data-ttu-id="7bec0-109">Das Cmdlet " **Get-AzRecoveryServicesAsrvCenter** " ruft Details zu den vCenter-Servern ab, die für die Ermittlung auf dem vom ASR-Fabric angegebenen Konfigurationsserver registriert sind.</span><span class="sxs-lookup"><span data-stu-id="7bec0-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="7bec0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bec0-110">EXAMPLES</span></span>

### <span data-ttu-id="7bec0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bec0-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="7bec0-112">Holen Sie sich Azure Site Recovery vCenter nach Fabric-Name und Name von vCenter.</span><span class="sxs-lookup"><span data-stu-id="7bec0-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="7bec0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7bec0-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="7bec0-114">Abrufen der Azure-Website-Wiederherstellungs-vCenter-Liste nach Fabric-Namen.</span><span class="sxs-lookup"><span data-stu-id="7bec0-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="7bec0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bec0-115">PARAMETERS</span></span>

### <span data-ttu-id="7bec0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bec0-116">-DefaultProfile</span></span>
<span data-ttu-id="7bec0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bec0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bec0-118">-Stoff</span><span class="sxs-lookup"><span data-stu-id="7bec0-118">-Fabric</span></span>
<span data-ttu-id="7bec0-119">ASR-Fabric-Objekt, das den Konfigurations Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bec0-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="7bec0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7bec0-120">-Name</span></span>
<span data-ttu-id="7bec0-121">Der Name des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="7bec0-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="7bec0-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7bec0-122">-ResourceId</span></span>
<span data-ttu-id="7bec0-123">Gibt die Resourcen-Nr von vCenter an.</span><span class="sxs-lookup"><span data-stu-id="7bec0-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="7bec0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bec0-124">CommonParameters</span></span>
<span data-ttu-id="7bec0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bec0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bec0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bec0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bec0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bec0-127">INPUTS</span></span>

### <span data-ttu-id="7bec0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7bec0-128">System.String</span></span>

### <span data-ttu-id="7bec0-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7bec0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7bec0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bec0-130">OUTPUTS</span></span>

### <span data-ttu-id="7bec0-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="7bec0-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="7bec0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bec0-132">NOTES</span></span>

## <span data-ttu-id="7bec0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bec0-133">RELATED LINKS</span></span>
