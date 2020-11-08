---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006629"
---
# <span data-ttu-id="b2c4f-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b2c4f-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="b2c4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c4f-103">Legt den Zustand für eine Website Wiederherstellungs Schutz Entität fest.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="b2c4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c4f-104">SYNTAX</span></span>

### <span data-ttu-id="b2c4f-105">ByPEObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2c4f-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c4f-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="b2c4f-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c4f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2c4f-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c4f-108">Das Cmdlet " **Satz-AzureSiteRecoveryProtectionEntity** " aktiviert oder deaktiviert den Schutz für eine Azure Site Recovery Protection-Entität.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="b2c4f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2c4f-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c4f-110">Beispiel 1: Aktivieren des Schutzes für Objekte in einem Container</span><span class="sxs-lookup"><span data-stu-id="b2c4f-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="b2c4f-111">Der erste Befehl ruft Container für den aktuellen Azure Site Vault mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert ihn dann in der $ProtectionContainer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="b2c4f-112">Der zweite Befehl ruft die geschützten virtuellen Computer ab, die zu dem in $ProtectionContainer gespeicherten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="b2c4f-113">Der Befehl speichert die Ergebnisse in der $ProtectionEntity-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="b2c4f-114">Der endgültige Befehl ermöglicht den Schutz für die in $ProtectionEntity gespeicherten Entitäten.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="b2c4f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c4f-115">PARAMETERS</span></span>

### <span data-ttu-id="b2c4f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b2c4f-116">-Force</span></span>
<span data-ttu-id="b2c4f-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2c4f-118">-ID</span><span class="sxs-lookup"><span data-stu-id="b2c4f-118">-Id</span></span>
<span data-ttu-id="b2c4f-119">Gibt die ID eines geschützten virtuellen Computers an, für den der Schutz aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4f-120">-OS</span><span class="sxs-lookup"><span data-stu-id="b2c4f-120">-OS</span></span>
<span data-ttu-id="b2c4f-121">Gibt den Typ des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-121">Specifies the operating system type.</span></span>
<span data-ttu-id="b2c4f-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2c4f-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2c4f-123">Windows</span><span class="sxs-lookup"><span data-stu-id="b2c4f-123">Windows</span></span>
- <span data-ttu-id="b2c4f-124">Linux</span><span class="sxs-lookup"><span data-stu-id="b2c4f-124">Linux</span></span>

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

### <span data-ttu-id="b2c4f-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="b2c4f-125">-OSDiskName</span></span>
<span data-ttu-id="b2c4f-126">Gibt den Namen des Datenträgers an, der das Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-126">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="b2c4f-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2c4f-127">-Profile</span></span>
<span data-ttu-id="b2c4f-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2c4f-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2c4f-130">-Schutz</span><span class="sxs-lookup"><span data-stu-id="b2c4f-130">-Protection</span></span>
<span data-ttu-id="b2c4f-131">Gibt an, ob der Schutz aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="b2c4f-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2c4f-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2c4f-133">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="b2c4f-133">Enable</span></span>
- <span data-ttu-id="b2c4f-134">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="b2c4f-134">Disable</span></span>

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

### <span data-ttu-id="b2c4f-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="b2c4f-135">-ProtectionContainerId</span></span>
<span data-ttu-id="b2c4f-136">Gibt die ID eines geschützten Containers an.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="b2c4f-137">Dieses Cmdlet aktiviert oder deaktiviert den Schutz für einen virtuellen Computer, der zu dem Container gehört, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4f-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b2c4f-138">-ProtectionEntity</span></span>
<span data-ttu-id="b2c4f-139">Gibt das Schutz Entitätsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-139">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="b2c4f-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4f-140">-ProtectionProfile</span></span>
<span data-ttu-id="b2c4f-141">Gibt ein Schutzprofil an, um den Schutz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="b2c4f-142">Geben Sie ein **ASRProtectionProfile** -Objekt an, das eines der verfügbaren Schutzprofile im zugehörigen Schutzcontainer ist.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4f-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b2c4f-143">-WaitForCompletion</span></span>
<span data-ttu-id="b2c4f-144">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b2c4f-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2c4f-145">-Confirm</span></span>
<span data-ttu-id="b2c4f-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c4f-147">-WhatIf</span></span>
<span data-ttu-id="b2c4f-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c4f-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c4f-150">CommonParameters</span></span>
<span data-ttu-id="b2c4f-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c4f-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c4f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c4f-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2c4f-153">INPUTS</span></span>

## <span data-ttu-id="b2c4f-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2c4f-154">OUTPUTS</span></span>

## <span data-ttu-id="b2c4f-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2c4f-155">NOTES</span></span>

## <span data-ttu-id="b2c4f-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2c4f-156">RELATED LINKS</span></span>

[<span data-ttu-id="b2c4f-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2c4f-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="b2c4f-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b2c4f-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="b2c4f-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b2c4f-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


