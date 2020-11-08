---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006606"
---
# <span data-ttu-id="56748-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="56748-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="56748-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56748-102">SYNOPSIS</span></span>
<span data-ttu-id="56748-103">Aktualisiert den Quell-und Zielserver zum Schutz eines Website Wiederherstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="56748-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="56748-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56748-104">SYNTAX</span></span>

### <span data-ttu-id="56748-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="56748-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="56748-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="56748-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="56748-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="56748-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="56748-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="56748-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56748-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56748-109">DESCRIPTION</span></span>
<span data-ttu-id="56748-110">Das Cmdlet **Update-AzureSiteRecoveryProtectionDirection** aktualisiert den Quell-und Zielserver zum Schutz eines Azure Site Recovery-Objekts nach Abschluss eines Commit-Failover-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="56748-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="56748-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56748-111">EXAMPLES</span></span>

### <span data-ttu-id="56748-112">Beispiel 1: Ändern der Richtung für ein geschütztes Objekt in einem Container</span><span class="sxs-lookup"><span data-stu-id="56748-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="56748-113">Der erste Befehl ruft die geschützten Container im aktuellen Azure Site Recovery Vault mithilfe des **Get-AzureSiteRecoveryProtectionContainer-** Cmdlets ab und speichert Sie dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="56748-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="56748-114">Der zweite Befehl ruft die virtuellen Computer ab, die zu dem in $Container gespeicherten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="56748-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="56748-115">Der Befehl speichert die Ergebnisse in der $protected-Variablen.</span><span class="sxs-lookup"><span data-stu-id="56748-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="56748-116">Der letzte Befehl legt die Richtung für die RecoverToPrimary für die in $Protected gespeicherten Objekte fest.</span><span class="sxs-lookup"><span data-stu-id="56748-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="56748-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="56748-117">PARAMETERS</span></span>

### <span data-ttu-id="56748-118">-Richtung</span><span class="sxs-lookup"><span data-stu-id="56748-118">-Direction</span></span>
<span data-ttu-id="56748-119">Gibt die Richtung des Commits an.</span><span class="sxs-lookup"><span data-stu-id="56748-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="56748-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="56748-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56748-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="56748-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="56748-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="56748-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="56748-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="56748-123">-Profile</span></span>
<span data-ttu-id="56748-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="56748-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56748-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="56748-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56748-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="56748-126">-ProtectionContainerId</span></span>
<span data-ttu-id="56748-127">Gibt die ID eines geschützten Containers an.</span><span class="sxs-lookup"><span data-stu-id="56748-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="56748-128">Dieses Cmdlet ändert die Richtung für einen geschützten virtuellen Computer, der zu dem Container gehört, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="56748-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56748-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56748-129">-ProtectionEntity</span></span>
<span data-ttu-id="56748-130">Gibt das Schutz Entitätsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="56748-130">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56748-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="56748-131">-ProtectionEntityId</span></span>
<span data-ttu-id="56748-132">Gibt die ID eines geschützten virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="56748-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="56748-133">Dieses Cmdlet ändert die Richtung für den geschützten virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="56748-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56748-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56748-134">-RecoveryPlan</span></span>
<span data-ttu-id="56748-135">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="56748-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56748-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="56748-136">-RPId</span></span>
<span data-ttu-id="56748-137">Gibt die ID eines Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="56748-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="56748-138">Dieses Cmdlet ändert die Richtung für den Wiederherstellungsplan, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="56748-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56748-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="56748-139">-WaitForCompletion</span></span>
<span data-ttu-id="56748-140">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="56748-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="56748-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56748-141">CommonParameters</span></span>
<span data-ttu-id="56748-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56748-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56748-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56748-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56748-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56748-144">INPUTS</span></span>

## <span data-ttu-id="56748-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56748-145">OUTPUTS</span></span>

## <span data-ttu-id="56748-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="56748-146">NOTES</span></span>

## <span data-ttu-id="56748-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56748-147">RELATED LINKS</span></span>

[<span data-ttu-id="56748-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="56748-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="56748-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56748-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


