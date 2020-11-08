---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006054"
---
# <span data-ttu-id="30a76-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="30a76-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="30a76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30a76-102">SYNOPSIS</span></span>
<span data-ttu-id="30a76-103">Startet einen Standort Wiederherstellungs-Replikationsrichtlinien Zuordnungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="30a76-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="30a76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a76-104">SYNTAX</span></span>

### <span data-ttu-id="30a76-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="30a76-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30a76-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="30a76-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30a76-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30a76-107">DESCRIPTION</span></span>
<span data-ttu-id="30a76-108">Das Cmdlet **Start-AzureSiteRecoveryProtectionProfileAssociationJob** initiiert einen Zuordnungs Auftrag, um eine Replikationsrichtlinie einem Azure Site Recovery Protection-Container zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="30a76-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="30a76-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30a76-109">EXAMPLES</span></span>

### <span data-ttu-id="30a76-110">Beispiel 1: Zuweisen eines Schutz Profils</span><span class="sxs-lookup"><span data-stu-id="30a76-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="30a76-111">Der erste Befehl ruft einen Schutzcontainer mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert diesen Container dann in der Variablen $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="30a76-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="30a76-112">Der zweite Befehl erstellt ein Schutzprofil mithilfe des Cmdlets **New-AzureSiteRecoveryProtectionProfileObject** und speichert dieses Schutzprofil in der $ProtectionProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="30a76-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="30a76-113">Der dritte Befehl ruft einen Schutzcontainer ab und speichert ihn dann in der Variablen $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="30a76-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="30a76-114">Der endgültige Befehl ordnet das in $ProtectionProfile gespeicherte Schutzprofil dem Container zu, der in $ProtectionContainer 01 als primärer Schutzcontainer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="30a76-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="30a76-115">Der Befehl ordnet den in $ProtectionContainer 02 gespeicherten Container als Wiederherstellungs Schutzcontainer zu.</span><span class="sxs-lookup"><span data-stu-id="30a76-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="30a76-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a76-116">PARAMETERS</span></span>

### <span data-ttu-id="30a76-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="30a76-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="30a76-118">Gibt den primären Schutzcontainer an, auf dem die Schutzprofil Einstellungen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30a76-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a76-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="30a76-119">-Profile</span></span>
<span data-ttu-id="30a76-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="30a76-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30a76-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="30a76-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30a76-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="30a76-122">-ProtectionProfile</span></span>
<span data-ttu-id="30a76-123">Gibt die Schutzprofil Einstellungen an, die auf die Schutzcontainer angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30a76-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="30a76-124">Verwenden Sie das New-AzureSiteRecoveryProtectionProfileObject-Cmdlet, um ein **ASRProtectionProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="30a76-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a76-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="30a76-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="30a76-126">Gibt den Wiederherstellungs Schutzcontainer an, auf dem die Schutzprofil Einstellungen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30a76-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a76-127">CommonParameters</span></span>
<span data-ttu-id="30a76-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a76-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30a76-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a76-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30a76-130">INPUTS</span></span>

## <span data-ttu-id="30a76-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30a76-131">OUTPUTS</span></span>

## <span data-ttu-id="30a76-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="30a76-132">NOTES</span></span>

## <span data-ttu-id="30a76-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30a76-133">RELATED LINKS</span></span>

[<span data-ttu-id="30a76-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="30a76-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="30a76-135">Neu – AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="30a76-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="30a76-136">Anfang-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="30a76-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


