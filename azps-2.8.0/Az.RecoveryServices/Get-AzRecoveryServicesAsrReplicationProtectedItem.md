---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824383"
---
# <span data-ttu-id="6e9ef-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6e9ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9ef-103">Ruft die Eigenschaften von geschützten Elementen einer Azure Site Recovery-Replikation ab.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="6e9ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e9ef-104">SYNTAX</span></span>

### <span data-ttu-id="6e9ef-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e9ef-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e9ef-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6e9ef-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e9ef-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6e9ef-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e9ef-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="6e9ef-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e9ef-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e9ef-109">DESCRIPTION</span></span>
<span data-ttu-id="6e9ef-110">Das Cmdlet " **Get-AzRecoveryServicesAsrReplicationProtectedItem** " Ruft die Eigenschaften aller oder des angegebenen ASR-Replikations geschützten Elements aus dem angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="6e9ef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e9ef-111">EXAMPLES</span></span>

### <span data-ttu-id="6e9ef-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6e9ef-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="6e9ef-113">Listet alle durch die Replikation geschützten Elemente im angegebenen ASR-Schutzcontainer auf.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="6e9ef-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e9ef-114">PARAMETERS</span></span>

### <span data-ttu-id="6e9ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9ef-115">-DefaultProfile</span></span>
<span data-ttu-id="6e9ef-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6e9ef-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6e9ef-117">-FriendlyName</span></span>
<span data-ttu-id="6e9ef-118">Gibt den Anzeigenamen des abzurufenden Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="6e9ef-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6e9ef-119">-Name</span></span>
<span data-ttu-id="6e9ef-120">Gibt den Namen des abzurufenden Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="6e9ef-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-121">-ProtectableItem</span></span>
<span data-ttu-id="6e9ef-122">Gibt ein geschütztes ASR-Element Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="6e9ef-123">Das Cmdlet ruft das geschützte ASR-Replikations Element ab, das dem angegebenen ASR-Schutzelement entspricht, wenn das Element geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9ef-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6e9ef-124">-ProtectionContainer</span></span>
<span data-ttu-id="6e9ef-125">Gibt das ASR-Schutzcontainer Objekt des ASR-Schutz Containers an, das dem geschützten Replikat Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9ef-126">CommonParameters</span></span>
<span data-ttu-id="6e9ef-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9ef-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9ef-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e9ef-129">INPUTS</span></span>

### <span data-ttu-id="6e9ef-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6e9ef-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="6e9ef-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="6e9ef-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e9ef-132">OUTPUTS</span></span>

### <span data-ttu-id="6e9ef-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6e9ef-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e9ef-134">NOTES</span></span>

## <span data-ttu-id="6e9ef-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e9ef-135">RELATED LINKS</span></span>

[<span data-ttu-id="6e9ef-136">Neu – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6e9ef-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6e9ef-138">Satz-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e9ef-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
