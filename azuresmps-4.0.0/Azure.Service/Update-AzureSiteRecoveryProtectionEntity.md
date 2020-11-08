---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006221"
---
# <span data-ttu-id="1f452-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1f452-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="1f452-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f452-102">SYNOPSIS</span></span>
<span data-ttu-id="1f452-103">Aktualisiert die Eigenschaften einer Schutz Entität in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1f452-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="1f452-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f452-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1f452-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f452-105">DESCRIPTION</span></span>
<span data-ttu-id="1f452-106">Das Cmdlet **Update-AzureSiteRecoveryProtectionEntity** aktualisiert die Eigenschaften einer Schutz Entität in Azure Site Recovery, wie etwa Besitzerinformationen des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1f452-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="1f452-107">Dieses Cmdlet wird nur für Virtual Machine Monitor (VMM) für VMM-geschützte Schutz Entitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f452-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="1f452-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f452-108">EXAMPLES</span></span>

### <span data-ttu-id="1f452-109">Beispiel 1: Aktualisieren einer Schutz Entität</span><span class="sxs-lookup"><span data-stu-id="1f452-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="1f452-110">Der erste Befehl ruft einen geschützten Container mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert dieses Objekt dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="1f452-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="1f452-111">Der zweite Befehl ruft den geschützten virtuellen Computer ab, der dem in $Container gespeicherten Container mit dem Cmdlet **Get-AzureSiteRecoveryProtectionEntity** zugeordnet ist, und speichert ihn dann in der Variablen $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="1f452-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="1f452-112">Der endgültige Befehl aktualisiert die Schutz Entität in $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="1f452-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="1f452-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f452-113">PARAMETERS</span></span>

### <span data-ttu-id="1f452-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="1f452-114">-Profile</span></span>
<span data-ttu-id="1f452-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1f452-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f452-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1f452-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f452-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1f452-117">-ProtectionEntity</span></span>
<span data-ttu-id="1f452-118">Gibt eine zu aktualisierende Schutz Entität an.</span><span class="sxs-lookup"><span data-stu-id="1f452-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="1f452-119">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryProtectionEntity** , um ein **ASRProtectionEntity** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1f452-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f452-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1f452-120">-WaitForCompletion</span></span>
<span data-ttu-id="1f452-121">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1f452-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="1f452-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f452-122">CommonParameters</span></span>
<span data-ttu-id="1f452-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f452-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f452-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f452-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f452-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f452-125">INPUTS</span></span>

## <span data-ttu-id="1f452-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f452-126">OUTPUTS</span></span>

## <span data-ttu-id="1f452-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f452-127">NOTES</span></span>

## <span data-ttu-id="1f452-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f452-128">RELATED LINKS</span></span>

[<span data-ttu-id="1f452-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1f452-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="1f452-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1f452-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="1f452-131">Satz-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1f452-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


