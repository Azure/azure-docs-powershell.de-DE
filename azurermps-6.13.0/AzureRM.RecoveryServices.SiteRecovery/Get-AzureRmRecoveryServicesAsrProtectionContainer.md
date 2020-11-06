---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6572fb6f98e06d03d698f75948ac4a7a38f2e785
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480178"
---
# <span data-ttu-id="f5007-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f5007-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f5007-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5007-102">SYNOPSIS</span></span>
<span data-ttu-id="f5007-103">Ruft ASR-Schutzcontainer im Speicher für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="f5007-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5007-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5007-104">SYNTAX</span></span>

### <span data-ttu-id="f5007-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5007-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5007-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f5007-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5007-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f5007-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5007-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5007-108">DESCRIPTION</span></span>
<span data-ttu-id="f5007-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrProtectionContainer** " ruft Azure Site Recovery Protection-Container im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="f5007-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="f5007-110">Ein Schutzcontainer ist ein logischer Container für schützende (erkannte) und geschützte Objekte wie virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="f5007-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="f5007-111">Replikationsrichtlinien definieren Replikationseinstellungen für geschützte Elemente und können einem Schutzcontainer zugeordnet und auf ein geschütztes Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5007-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="f5007-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5007-112">EXAMPLES</span></span>

### <span data-ttu-id="f5007-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5007-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="f5007-114">Liste der Schutzcontainer in Fabric-$Fabric.</span><span class="sxs-lookup"><span data-stu-id="f5007-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="f5007-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f5007-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="f5007-116">Schutzcontainer in Stoff $fabric mit Namen.</span><span class="sxs-lookup"><span data-stu-id="f5007-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="f5007-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f5007-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="f5007-118">Schutzcontainer in Stoff $fabric mit Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="f5007-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="f5007-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5007-119">PARAMETERS</span></span>

### <span data-ttu-id="f5007-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5007-120">-DefaultProfile</span></span>
<span data-ttu-id="f5007-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5007-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f5007-122">-Stoff</span><span class="sxs-lookup"><span data-stu-id="f5007-122">-Fabric</span></span>
<span data-ttu-id="f5007-123">Suchen Sie im angegebenen ASR-Fabric nach dem Schutzcontainer.</span><span class="sxs-lookup"><span data-stu-id="f5007-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5007-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f5007-124">-FriendlyName</span></span>
<span data-ttu-id="f5007-125">Gibt den Anzeigenamen des ASR-Schutz Containers an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5007-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5007-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f5007-126">-Name</span></span>
<span data-ttu-id="f5007-127">Gibt den Namen des ASR-Schutz Containers an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5007-127">Specifies the name of the ASR protection container to look for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5007-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5007-128">CommonParameters</span></span>
<span data-ttu-id="f5007-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5007-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5007-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5007-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5007-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5007-131">INPUTS</span></span>

### <span data-ttu-id="f5007-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f5007-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f5007-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5007-133">OUTPUTS</span></span>

### <span data-ttu-id="f5007-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f5007-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f5007-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5007-135">NOTES</span></span>

## <span data-ttu-id="f5007-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5007-136">RELATED LINKS</span></span>
