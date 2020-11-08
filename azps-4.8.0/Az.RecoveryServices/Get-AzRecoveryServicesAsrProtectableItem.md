---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166178"
---
# <span data-ttu-id="590a7-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="590a7-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="590a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="590a7-102">SYNOPSIS</span></span>
<span data-ttu-id="590a7-103">Rufen Sie die geschützten Elemente in einem ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="590a7-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="590a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="590a7-104">SYNTAX</span></span>

### <span data-ttu-id="590a7-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="590a7-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590a7-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="590a7-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590a7-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="590a7-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="590a7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="590a7-108">DESCRIPTION</span></span>
<span data-ttu-id="590a7-109">Das Cmdlet " **Get-AzRecoveryServicesAsrProtectableItem** " Ruft die geschützten Elemente in einem Azure Site Recovery Protection-Container ab.</span><span class="sxs-lookup"><span data-stu-id="590a7-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="590a7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="590a7-110">EXAMPLES</span></span>

### <span data-ttu-id="590a7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="590a7-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="590a7-112">Ruft alle geschützten Elemente im angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="590a7-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="590a7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="590a7-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="590a7-114">Besorgen Sie sich die geschützten Elemente im angegebenen ASR-Schutzcontainer und mit dem angegebenen Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="590a7-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="590a7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="590a7-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="590a7-116">Ruft alle geschützten Elemente im angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="590a7-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="590a7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="590a7-117">PARAMETERS</span></span>

### <span data-ttu-id="590a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590a7-118">-DefaultProfile</span></span>
<span data-ttu-id="590a7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="590a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="590a7-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="590a7-120">-FriendlyName</span></span>
<span data-ttu-id="590a7-121">Gibt den Anzeigenamen des ASR-geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="590a7-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="590a7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="590a7-122">-Name</span></span>
<span data-ttu-id="590a7-123">Gibt den Namen des ASR-geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="590a7-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="590a7-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="590a7-124">-ProtectionContainer</span></span>
<span data-ttu-id="590a7-125">Gibt das Azure Site Recovery Protection-Container Objekt an.</span><span class="sxs-lookup"><span data-stu-id="590a7-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="590a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590a7-126">CommonParameters</span></span>
<span data-ttu-id="590a7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590a7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="590a7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590a7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="590a7-129">INPUTS</span></span>

### <span data-ttu-id="590a7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="590a7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="590a7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="590a7-131">OUTPUTS</span></span>

### <span data-ttu-id="590a7-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="590a7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="590a7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="590a7-133">NOTES</span></span>

## <span data-ttu-id="590a7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="590a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="590a7-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="590a7-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="590a7-136">Satz-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="590a7-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
