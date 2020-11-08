---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005960"
---
# <span data-ttu-id="2e2c6-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="2e2c6-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="2e2c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2c6-103">Legt die Wiederherstellungs seitigen Optionen für eine Website Wiederherstellungs Schutz Entität fest.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="2e2c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e2c6-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e2c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e2c6-105">DESCRIPTION</span></span>
<span data-ttu-id="2e2c6-106">Das Cmdlet " **Set-AzureSiteRecoveryVM** " legt die Optionen für den Wiederherstellungs seitigen Schutz fest, beispielsweise die Größe der Wiederherstellungs-und Wiederherstellungs-Virtual Machine-Netzwerk für Azure Site Recovery Protection-Entitäten.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="2e2c6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e2c6-107">EXAMPLES</span></span>

### <span data-ttu-id="2e2c6-108">Beispiel 1: zulassen des Updates auf einem geschützten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="2e2c6-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="2e2c6-109">Der erste Befehl verwendet das Cmdlet " **Get-AzureSiteRecoveryProtectionContainer** ", um einen geschützten Container abzurufen, und speichert ihn dann in der $ProtectionContainer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="2e2c6-110">Der zweite Befehl ruft die virtuellen Computer in $ProtectionContainer mit dem Cmdlet **Get-AzureSiteRecoveryVM** ab und speichert Sie dann in der Variablen $VitrualMachines.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="2e2c6-111">Der endgültige Befehl ermöglicht Updates für den ersten virtuellen Computer im $VitrualMachines-Array mit dem Namen NewVirtualMachine05.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="2e2c6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e2c6-112">PARAMETERS</span></span>

### <span data-ttu-id="2e2c6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2e2c6-113">-Name</span></span>
<span data-ttu-id="2e2c6-114">Gibt den Namen der virtuellen Zielmaschine an.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-114">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="2e2c6-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="2e2c6-115">-PrimaryNic</span></span>
<span data-ttu-id="2e2c6-116">Gibt die primäre Netzwerkadapterkarte an.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-116">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="2e2c6-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="2e2c6-117">-Profile</span></span>
<span data-ttu-id="2e2c6-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e2c6-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e2c6-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="2e2c6-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="2e2c6-121">Gibt die Wiederherstellungs Netzwerk-ID an.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-121">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="2e2c6-122">-Size</span><span class="sxs-lookup"><span data-stu-id="2e2c6-122">-Size</span></span>
<span data-ttu-id="2e2c6-123">Gibt die Größe des virtuellen Zielcomputers an.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-123">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="2e2c6-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2e2c6-124">-VirtualMachine</span></span>
<span data-ttu-id="2e2c6-125">Gibt das Objekt für den virtuellen Computer der Websitewiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2c6-126">CommonParameters</span></span>
<span data-ttu-id="2e2c6-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2c6-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e2c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2c6-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e2c6-129">INPUTS</span></span>

## <span data-ttu-id="2e2c6-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e2c6-130">OUTPUTS</span></span>

## <span data-ttu-id="2e2c6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e2c6-131">NOTES</span></span>

## <span data-ttu-id="2e2c6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e2c6-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e2c6-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2e2c6-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="2e2c6-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="2e2c6-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


