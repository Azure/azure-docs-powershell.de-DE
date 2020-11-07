---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664711"
---
# <span data-ttu-id="b896f-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b896f-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="b896f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b896f-102">SYNOPSIS</span></span>
<span data-ttu-id="b896f-103">Erstellt eine Replikationsrichtlinie für die Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="b896f-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b896f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b896f-104">SYNTAX</span></span>

### <span data-ttu-id="b896f-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="b896f-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b896f-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b896f-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b896f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b896f-107">DESCRIPTION</span></span>
<span data-ttu-id="b896f-108">Das Cmdlet **New-AzureRmSiteRecoveryPolicy** erstellt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b896f-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="b896f-109">Die Replikationsrichtlinie wird verwendet, um Replikationseinstellungen wie die Replikationshäufigkeit und die Anzahl der Wiederherstellungspunkte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b896f-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="b896f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b896f-110">EXAMPLES</span></span>

## <span data-ttu-id="b896f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b896f-111">PARAMETERS</span></span>

### <span data-ttu-id="b896f-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b896f-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="b896f-113">Gibt die Häufigkeit des konsistenten Snapshots der Anwendung in Stunden an.</span><span class="sxs-lookup"><span data-stu-id="b896f-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-114">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="b896f-114">-Authentication</span></span>
<span data-ttu-id="b896f-115">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="b896f-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="b896f-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b896f-116">Valid values are:</span></span>

- <span data-ttu-id="b896f-117">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="b896f-117">Certificate</span></span>
-  <span data-ttu-id="b896f-118">Kerberos</span><span class="sxs-lookup"><span data-stu-id="b896f-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-119">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="b896f-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-120">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="b896f-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b896f-121">-Name</span></span>
<span data-ttu-id="b896f-122">Gibt einen Anzeigenamen an, der die Replikationsrichtlinie für die Standortwiederherstellung kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="b896f-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="b896f-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b896f-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b896f-124">Gibt die Azure-Speicherkonto-ID des Replikations Ziels an.</span><span class="sxs-lookup"><span data-stu-id="b896f-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="b896f-125">-RecoveryPoints</span></span>
<span data-ttu-id="b896f-126">Gibt die Anzahl von Stunden an, um Wiederherstellungspunkte beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b896f-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="b896f-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="b896f-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="b896f-129">Gibt das Replikations Häufigkeitsintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b896f-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="b896f-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b896f-130">Valid values are:</span></span>

- <span data-ttu-id="b896f-131">30</span><span class="sxs-lookup"><span data-stu-id="b896f-131">30</span></span>
- <span data-ttu-id="b896f-132">300</span><span class="sxs-lookup"><span data-stu-id="b896f-132">300</span></span>
- <span data-ttu-id="b896f-133">900</span><span class="sxs-lookup"><span data-stu-id="b896f-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="b896f-134">-ReplicationMethod</span></span>
<span data-ttu-id="b896f-135">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="b896f-135">Specifies the replication method.</span></span>
<span data-ttu-id="b896f-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b896f-136">Valid values are:</span></span>

- <span data-ttu-id="b896f-137">Online</span><span class="sxs-lookup"><span data-stu-id="b896f-137">Online</span></span>
- <span data-ttu-id="b896f-138">Offline</span><span class="sxs-lookup"><span data-stu-id="b896f-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="b896f-139">-ReplicationPort</span></span>
<span data-ttu-id="b896f-140">Gibt den Port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b896f-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="b896f-141">-ReplicationProvider</span></span>
<span data-ttu-id="b896f-142">Gibt den Replikationsanbieter an.</span><span class="sxs-lookup"><span data-stu-id="b896f-142">Specifies the replication provider.</span></span>
<span data-ttu-id="b896f-143">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b896f-143">Valid values are:</span></span>

- <span data-ttu-id="b896f-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="b896f-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="b896f-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="b896f-145">HyperVReplica2012</span></span>
- <span data-ttu-id="b896f-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="b896f-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="b896f-147">-ReplicationStartTime</span></span>
<span data-ttu-id="b896f-148">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="b896f-148">Specifies the replication start time.</span></span>
<span data-ttu-id="b896f-149">Sie darf nicht später als 24 Stunden nach dem Start des Auftrags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b896f-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b896f-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b896f-150">-DefaultProfile</span></span>
<span data-ttu-id="b896f-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b896f-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b896f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b896f-152">CommonParameters</span></span>
<span data-ttu-id="b896f-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b896f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b896f-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b896f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b896f-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b896f-155">INPUTS</span></span>

## <span data-ttu-id="b896f-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b896f-156">OUTPUTS</span></span>

## <span data-ttu-id="b896f-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="b896f-157">NOTES</span></span>

## <span data-ttu-id="b896f-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b896f-158">RELATED LINKS</span></span>

[<span data-ttu-id="b896f-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b896f-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="b896f-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b896f-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
