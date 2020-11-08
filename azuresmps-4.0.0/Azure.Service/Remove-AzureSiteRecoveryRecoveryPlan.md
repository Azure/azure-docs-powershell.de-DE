---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006317"
---
# <span data-ttu-id="66464-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66464-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="66464-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66464-102">SYNOPSIS</span></span>
<span data-ttu-id="66464-103">Entfernt einen Website Wiederherstellungsplan aus der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="66464-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="66464-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66464-104">SYNTAX</span></span>

### <span data-ttu-id="66464-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="66464-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66464-106">ById</span><span class="sxs-lookup"><span data-stu-id="66464-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66464-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66464-107">DESCRIPTION</span></span>
<span data-ttu-id="66464-108">Das Cmdlet **Remove-AzureSiteRecoveryRecoveryPlan** entfernt einen Website Wiederherstellungsplan aus der aktuellen Azure Site-Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="66464-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="66464-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66464-109">EXAMPLES</span></span>

### <span data-ttu-id="66464-110">Beispiel 1: Entfernen eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="66464-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="66464-111">Der erste Befehl verwendet das Cmdlet " **Get-AzureSiteRecoveryRecoveryPlan** ", um den Website Wiederherstellungsplan abzurufen, und speichert ihn dann in der $RecoveryPlan-Variablen.</span><span class="sxs-lookup"><span data-stu-id="66464-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="66464-112">Der zweite Befehl entfernt den Wiederherstellungsplan in $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="66464-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="66464-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="66464-113">PARAMETERS</span></span>

### <span data-ttu-id="66464-114">-Force</span><span class="sxs-lookup"><span data-stu-id="66464-114">-Force</span></span>
<span data-ttu-id="66464-115">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="66464-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66464-116">-ID</span><span class="sxs-lookup"><span data-stu-id="66464-116">-Id</span></span>
<span data-ttu-id="66464-117">Gibt die ID des Wiederherstellungsplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66464-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66464-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="66464-118">-Profile</span></span>
<span data-ttu-id="66464-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="66464-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66464-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="66464-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66464-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66464-121">-RecoveryPlan</span></span>
<span data-ttu-id="66464-122">Gibt den Wiederherstellungsplan an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66464-122">Specifies the recovery plan to remove.</span></span>

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

### <span data-ttu-id="66464-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="66464-123">-WaitForCompletion</span></span>
<span data-ttu-id="66464-124">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="66464-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="66464-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66464-125">-Confirm</span></span>
<span data-ttu-id="66464-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66464-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66464-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66464-127">-WhatIf</span></span>
<span data-ttu-id="66464-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66464-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66464-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66464-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66464-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66464-130">CommonParameters</span></span>
<span data-ttu-id="66464-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66464-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66464-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66464-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66464-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66464-133">INPUTS</span></span>

## <span data-ttu-id="66464-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66464-134">OUTPUTS</span></span>

## <span data-ttu-id="66464-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="66464-135">NOTES</span></span>

## <span data-ttu-id="66464-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66464-136">RELATED LINKS</span></span>

[<span data-ttu-id="66464-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66464-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="66464-138">Neu – AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66464-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="66464-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="66464-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


