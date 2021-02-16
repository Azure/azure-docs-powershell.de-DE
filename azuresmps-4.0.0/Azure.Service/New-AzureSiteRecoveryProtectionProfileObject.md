---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403645"
---
# <span data-ttu-id="8d28f-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="8d28f-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="8d28f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d28f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d28f-103">Erstellt ein Profilobjekt für den Websitewiederherstellungsschutz.</span><span class="sxs-lookup"><span data-stu-id="8d28f-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="8d28f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d28f-104">SYNTAX</span></span>

### <span data-ttu-id="8d28f-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d28f-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8d28f-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8d28f-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8d28f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d28f-107">DESCRIPTION</span></span>
<span data-ttu-id="8d28f-108">Das **Cmdlet "New-AzureSiteRecoveryProtectionProfileObject"** erstellt ein Profilobjekt für den Azure-Websitewiederherstellungsschutz.</span><span class="sxs-lookup"><span data-stu-id="8d28f-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="8d28f-109">Dieses Cmdlet erstellt ein **ASRProtectionProfile-Objekt** zur Verwendung mit anderen Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8d28f-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="8d28f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d28f-110">EXAMPLES</span></span>

### <span data-ttu-id="8d28f-111">Beispiel 1: Erstellen eines Schutzprofils</span><span class="sxs-lookup"><span data-stu-id="8d28f-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="8d28f-112">Mit diesem Befehl wird ein Schutzprofilobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d28f-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="8d28f-113">Beispiel 2: Erstellen eines Schutzprofils für den HyperVReplicaAzure-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8d28f-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="8d28f-114">Mit diesem Befehl wird ein Schutzprofil für einen HyperVReplicaAzure-Anbieter erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d28f-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="8d28f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d28f-115">PARAMETERS</span></span>

### <span data-ttu-id="8d28f-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="8d28f-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="8d28f-117">Gibt an, dass das Schutzprofil das Löschen von Replikatentitäten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8d28f-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="8d28f-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8d28f-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="8d28f-119">Gibt die Häufigkeit (in Stunden) für konsistente Momentaufnahmen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="8d28f-120">-Authentication</span><span class="sxs-lookup"><span data-stu-id="8d28f-120">-Authentication</span></span>
<span data-ttu-id="8d28f-121">Gibt den zu verwendenden Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="8d28f-122">Die zulässigen Werte für diesen Parameter sind: "Certificate" und "Kerberos".</span><span class="sxs-lookup"><span data-stu-id="8d28f-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="8d28f-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="8d28f-123">-CompressionEnabled</span></span>
<span data-ttu-id="8d28f-124">Gibt an, dass das Schutzprofil die Komprimierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8d28f-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="8d28f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8d28f-125">-Force</span></span>
<span data-ttu-id="8d28f-126">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="8d28f-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d28f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8d28f-127">-Name</span></span>
<span data-ttu-id="8d28f-128">Gibt einen Namen für das Schutzprofil an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="8d28f-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="8d28f-129">-Profile</span></span>
<span data-ttu-id="8d28f-130">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8d28f-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d28f-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8d28f-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d28f-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d28f-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="8d28f-133">Gibt den Namen eines Azure Storage-Kontos an, in dem die Entität der Azure-Replikate gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d28f-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="8d28f-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8d28f-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="8d28f-135">Gibt die ID für ein Azure-Abonnement für ein Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="8d28f-136">Dieser Parameter bezieht sich auf das Konto, für das die Entität der Azure-Replikate gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d28f-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="8d28f-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="8d28f-137">-RecoveryPoints</span></span>
<span data-ttu-id="8d28f-138">Gibt die Anzahl der Stunden für die Aufbewahrung von Wiederherstellungspunkten an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="8d28f-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="8d28f-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="8d28f-140">Gibt das Häufigkeitsintervall für die Replikation in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="8d28f-141">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="8d28f-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d28f-142">30</span><span class="sxs-lookup"><span data-stu-id="8d28f-142">30</span></span> 
- <span data-ttu-id="8d28f-143">300</span><span class="sxs-lookup"><span data-stu-id="8d28f-143">300</span></span> 
- <span data-ttu-id="8d28f-144">900</span><span class="sxs-lookup"><span data-stu-id="8d28f-144">900</span></span>

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

### <span data-ttu-id="8d28f-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="8d28f-145">-ReplicationMethod</span></span>
<span data-ttu-id="8d28f-146">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-146">Specifies the replication method.</span></span> <span data-ttu-id="8d28f-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="8d28f-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d28f-148">Online.</span><span class="sxs-lookup"><span data-stu-id="8d28f-148">Online.</span></span>
<span data-ttu-id="8d28f-149">Replikation über das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8d28f-149">Replication over the network.</span></span>
- <span data-ttu-id="8d28f-150">"Offline" aus.</span><span class="sxs-lookup"><span data-stu-id="8d28f-150">Offline.</span></span>

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

### <span data-ttu-id="8d28f-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="8d28f-151">-ReplicationPort</span></span>
<span data-ttu-id="8d28f-152">Gibt die Nummer des Ports an, für den die Replikation erfolgt.</span><span class="sxs-lookup"><span data-stu-id="8d28f-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="8d28f-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="8d28f-153">-ReplicationProvider</span></span>
<span data-ttu-id="8d28f-154">Gibt den Typ des Replikationsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="8d28f-155">Die zulässigen Werte für diesen Parameter sind: HyperVReplica und HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="8d28f-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="8d28f-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="8d28f-156">-ReplicationStartTime</span></span>
<span data-ttu-id="8d28f-157">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="8d28f-158">Geben Sie eine Uhrzeit innerhalb von 24 Stunden nach dem Start des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="8d28f-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="8d28f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d28f-159">CommonParameters</span></span>
<span data-ttu-id="8d28f-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d28f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d28f-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d28f-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d28f-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d28f-162">INPUTS</span></span>

## <span data-ttu-id="8d28f-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d28f-163">OUTPUTS</span></span>

## <span data-ttu-id="8d28f-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8d28f-164">NOTES</span></span>

## <span data-ttu-id="8d28f-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8d28f-165">RELATED LINKS</span></span>




