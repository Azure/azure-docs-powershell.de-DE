---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006097"
---
# <span data-ttu-id="3233c-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="3233c-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="3233c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3233c-102">SYNOPSIS</span></span>
<span data-ttu-id="3233c-103">Erstellt ein Profilobjekt für einen Website Wiederherstellungs Schutz.</span><span class="sxs-lookup"><span data-stu-id="3233c-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="3233c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3233c-104">SYNTAX</span></span>

### <span data-ttu-id="3233c-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="3233c-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3233c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3233c-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3233c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3233c-107">DESCRIPTION</span></span>
<span data-ttu-id="3233c-108">Das Cmdlet **New-AzureSiteRecoveryProtectionProfileObject** erstellt ein Azure Site Recovery Protection-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="3233c-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="3233c-109">Mit diesem Cmdlet wird ein **ASRProtectionProfile** -Objekt erstellt, das mit anderen Cmdlets verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3233c-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="3233c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3233c-110">EXAMPLES</span></span>

### <span data-ttu-id="3233c-111">Beispiel 1: Erstellen eines Schutz Profils</span><span class="sxs-lookup"><span data-stu-id="3233c-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="3233c-112">Mit diesem Befehl wird ein Schutzprofil Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="3233c-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="3233c-113">Beispiel 2: Erstellen eines Schutz Profils für HyperVReplicaAzure-Anbieter</span><span class="sxs-lookup"><span data-stu-id="3233c-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="3233c-114">Dieser Befehl erstellt ein Schutzprofil für einen HyperVReplicaAzure-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3233c-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="3233c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3233c-115">PARAMETERS</span></span>

### <span data-ttu-id="3233c-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="3233c-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="3233c-117">Gibt an, dass das Schutzprofil das Löschen von Replikat Entitäten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3233c-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="3233c-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="3233c-119">Gibt die Häufigkeit in Stunden für anwendungskonsistente Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="3233c-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-120">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3233c-120">-Authentication</span></span>
<span data-ttu-id="3233c-121">Gibt den Typ der zu verwendenden Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="3233c-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="3233c-122">Die zulässigen Werte für diesen Parameter lauten: Certificate und Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3233c-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="3233c-123">-CompressionEnabled</span></span>
<span data-ttu-id="3233c-124">Gibt an, dass das Schutzprofil Komprimierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3233c-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3233c-125">-Force</span></span>
<span data-ttu-id="3233c-126">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3233c-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3233c-127">-Name</span></span>
<span data-ttu-id="3233c-128">Gibt einen Namen für das Schutzprofil an.</span><span class="sxs-lookup"><span data-stu-id="3233c-128">Specifies a name for the protection profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="3233c-129">-Profile</span></span>
<span data-ttu-id="3233c-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3233c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3233c-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3233c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3233c-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="3233c-133">Gibt den Namen eines Azure-speicherkontos an, auf dem die Azure Replica-Entität gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3233c-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3233c-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="3233c-135">Gibt die ID für ein Azure-Abonnement für ein Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="3233c-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="3233c-136">Dieser Parameter bezieht sich auf das Konto, für das die Azure Replica-Entität gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3233c-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="3233c-137">-RecoveryPoints</span></span>
<span data-ttu-id="3233c-138">Gibt die Anzahl von Stunden an, um Wiederherstellungspunkte beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3233c-138">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="3233c-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="3233c-140">Gibt das Häufigkeitsintervall für die Replikation in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="3233c-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="3233c-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3233c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3233c-142">30</span><span class="sxs-lookup"><span data-stu-id="3233c-142">30</span></span> 
- <span data-ttu-id="3233c-143">300</span><span class="sxs-lookup"><span data-stu-id="3233c-143">300</span></span> 
- <span data-ttu-id="3233c-144">900</span><span class="sxs-lookup"><span data-stu-id="3233c-144">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="3233c-145">-ReplicationMethod</span></span>
<span data-ttu-id="3233c-146">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="3233c-146">Specifies the replication method.</span></span> <span data-ttu-id="3233c-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3233c-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3233c-148">Online.</span><span class="sxs-lookup"><span data-stu-id="3233c-148">Online.</span></span>
<span data-ttu-id="3233c-149">Replikation über das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3233c-149">Replication over the network.</span></span>
- <span data-ttu-id="3233c-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="3233c-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="3233c-151">-ReplicationPort</span></span>
<span data-ttu-id="3233c-152">Gibt die Nummer des Ports an, auf dem die Replikation stattfindet.</span><span class="sxs-lookup"><span data-stu-id="3233c-152">Specifies the number of the port on which the replication occurs.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="3233c-153">-ReplicationProvider</span></span>
<span data-ttu-id="3233c-154">Gibt den Typ des Replikations Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="3233c-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="3233c-155">Die zulässigen Werte für diesen Parameter sind: HyperVReplica und HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="3233c-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="3233c-156">-ReplicationStartTime</span></span>
<span data-ttu-id="3233c-157">Gibt den Startzeitpunkt der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="3233c-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="3233c-158">Geben Sie eine Uhrzeit innerhalb von 24 Stunden nach dem Start des Auftrags ein.</span><span class="sxs-lookup"><span data-stu-id="3233c-158">Specify a time within 24 hours after you start the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3233c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3233c-159">CommonParameters</span></span>
<span data-ttu-id="3233c-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3233c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3233c-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3233c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3233c-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3233c-162">INPUTS</span></span>

## <span data-ttu-id="3233c-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3233c-163">OUTPUTS</span></span>

## <span data-ttu-id="3233c-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="3233c-164">NOTES</span></span>

## <span data-ttu-id="3233c-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3233c-165">RELATED LINKS</span></span>

[<span data-ttu-id="3233c-166">Azure Site Recovery Services-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3233c-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


