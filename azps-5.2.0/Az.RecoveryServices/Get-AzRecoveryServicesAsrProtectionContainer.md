---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307675"
---
# <span data-ttu-id="bed11-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="bed11-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="bed11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed11-102">SYNOPSIS</span></span>
<span data-ttu-id="bed11-103">Ruft DIE ASR-Schutzcontainer im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="bed11-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="bed11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bed11-104">SYNTAX</span></span>

### <span data-ttu-id="bed11-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="bed11-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bed11-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="bed11-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed11-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bed11-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed11-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bed11-108">DESCRIPTION</span></span>
<span data-ttu-id="bed11-109">Das **Cmdlet "Get-AzRecoveryServicesAsrProtectionContainer"** ruft Container für den Azure Site Recovery Protection im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="bed11-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="bed11-110">Ein Schutzcontainer ist ein logischer Container für schutzfähige (ermittelte) und geschützte Objekte wie virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="bed11-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="bed11-111">Replikationsrichtlinien definieren Replikationseinstellungen für geschützte Elemente und können einem Schutzcontainer zugeordnet und auf ein schützendes Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="bed11-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="bed11-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bed11-112">EXAMPLES</span></span>

### <span data-ttu-id="bed11-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bed11-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="bed11-114">List of protection container in fabric $fabric.</span><span class="sxs-lookup"><span data-stu-id="bed11-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="bed11-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bed11-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="bed11-116">Protection container in fabric $fabric with name.</span><span class="sxs-lookup"><span data-stu-id="bed11-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="bed11-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bed11-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="bed11-118">Protection container in fabric $fabric with friendly Name.</span><span class="sxs-lookup"><span data-stu-id="bed11-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="bed11-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bed11-119">PARAMETERS</span></span>

### <span data-ttu-id="bed11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed11-120">-DefaultProfile</span></span>
<span data-ttu-id="bed11-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bed11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bed11-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="bed11-122">-Fabric</span></span>
<span data-ttu-id="bed11-123">Suchen Sie nach dem Schutzcontainer in der angegebenen ASR-Struktur.</span><span class="sxs-lookup"><span data-stu-id="bed11-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="bed11-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bed11-124">-FriendlyName</span></span>
<span data-ttu-id="bed11-125">Gibt den Anzeigenamen des ASR-Schutzcontainers an, nach dem sie suchen soll.</span><span class="sxs-lookup"><span data-stu-id="bed11-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="bed11-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bed11-126">-Name</span></span>
<span data-ttu-id="bed11-127">Gibt den Namen des ASR-Schutzcontainers an, nach dem sie suchen soll.</span><span class="sxs-lookup"><span data-stu-id="bed11-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="bed11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed11-128">CommonParameters</span></span>
<span data-ttu-id="bed11-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed11-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bed11-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed11-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bed11-131">INPUTS</span></span>

### <span data-ttu-id="bed11-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bed11-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bed11-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bed11-133">OUTPUTS</span></span>

### <span data-ttu-id="bed11-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="bed11-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="bed11-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bed11-135">NOTES</span></span>

## <span data-ttu-id="bed11-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bed11-136">RELATED LINKS</span></span>
