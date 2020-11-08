---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006616"
---
# <span data-ttu-id="ba6a3-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="ba6a3-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="ba6a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6a3-103">Startet einen Dissoziation-Auftrag für eine Replikationsrichtlinie, die einem Schutzcontainer für die Standortwiederherstellung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="ba6a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba6a3-104">SYNTAX</span></span>

### <span data-ttu-id="ba6a3-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba6a3-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ba6a3-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ba6a3-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ba6a3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="ba6a3-108">Das Cmdlet **Start-AzureSiteRecoveryProtectionProfileDissociationJob** initiiert einen Dissoziation-Auftrag in der Replikationsrichtlinie, die einem Azure Site Recovery Protection-Container zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="ba6a3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba6a3-109">EXAMPLES</span></span>

### <span data-ttu-id="ba6a3-110">Beispiel 1: Trennen eines Schutz Profils</span><span class="sxs-lookup"><span data-stu-id="ba6a3-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="ba6a3-111">Der erste Befehl ruft einen Schutzcontainer mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert diesen Container dann in der Variablen $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="ba6a3-112">Der zweite Befehl ruft einen Schutzcontainer ab und speichert ihn dann in der Variablen $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="ba6a3-113">Der endgültige Befehl distanziert sich vom Schutzprofil des in $ProtectionContainer 01 gespeicherten Containers als primärer Schutzcontainer.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="ba6a3-114">Der Befehl distanziert den in $ProtectionContainer 02 gespeicherten Container als Wiederherstellungs Schutzcontainer.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="ba6a3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba6a3-115">PARAMETERS</span></span>

### <span data-ttu-id="ba6a3-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ba6a3-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="ba6a3-117">Gibt einen primären Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="ba6a3-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ba6a3-118">-Profile</span></span>
<span data-ttu-id="ba6a3-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba6a3-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba6a3-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="ba6a3-121">-ProtectionProfile</span></span>
<span data-ttu-id="ba6a3-122">Gibt die Schutzprofil Einstellungen an, mit denen die Zuordnung zu den Schutz Containern aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="ba6a3-123">Gibt die Schutzprofil Einstellungen an, die auf die Schutzcontainer angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="ba6a3-124">Verwenden Sie das New-AzureSiteRecoveryProtectionProfileObject-Cmdlet, um ein **ASRProtectionProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="ba6a3-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ba6a3-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="ba6a3-126">Gibt einen Wiederherstellungs Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="ba6a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6a3-127">CommonParameters</span></span>
<span data-ttu-id="ba6a3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6a3-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba6a3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6a3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba6a3-130">INPUTS</span></span>

## <span data-ttu-id="ba6a3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba6a3-131">OUTPUTS</span></span>

## <span data-ttu-id="ba6a3-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba6a3-132">NOTES</span></span>

## <span data-ttu-id="ba6a3-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba6a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba6a3-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ba6a3-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ba6a3-135">Neu – AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="ba6a3-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="ba6a3-136">Anfang-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="ba6a3-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


