---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006316"
---
# <span data-ttu-id="e0913-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e0913-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="e0913-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0913-102">SYNOPSIS</span></span>
<span data-ttu-id="e0913-103">Entfernt eine Netzwerkzuordnung aus einem Website Wiederherstellungs Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0913-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="e0913-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0913-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0913-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0913-105">DESCRIPTION</span></span>
<span data-ttu-id="e0913-106">Das Cmdlet **Remove-AzureSiteRecoveryNetworkMapping** entfernt eine Netzwerkzuordnung aus dem aktuellen Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="e0913-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e0913-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0913-107">EXAMPLES</span></span>

### <span data-ttu-id="e0913-108">Beispiel 1: Entfernen der Zuordnung zwischen einem Netzwerk und einem Wiederherstellungs Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e0913-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="e0913-109">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="e0913-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="e0913-110">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="e0913-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="e0913-111">Der zweite Befehl ruft die Zuordnung zwischen dem primären Netzwerk und dem Wiederherstellungs Netzwerk ab und speichert ihn dann in der $NetworkMapping Variablen.</span><span class="sxs-lookup"><span data-stu-id="e0913-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="e0913-112">Der Befehl gibt den primären Server für die Netzwerkzuordnung als erstes Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="e0913-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="e0913-113">Der Befehl gibt den Server für das Wiederherstellungs Netzwerk als zweites Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="e0913-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="e0913-114">Der endgültige Befehl entfernt die Netzwerkzuordnung in $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="e0913-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="e0913-115">Beispiel 2: Entfernen der Zuordnung zwischen einem Netzwerk und einem Azure Virtual Machine-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e0913-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="e0913-116">Das Cmdlet "erster Befehl" Ruft Server für den aktuellen Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="e0913-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="e0913-117">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="e0913-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="e0913-118">Der zweite Befehl ruft eine Zuordnung zwischen dem primären Netzwerk und einem Azure Virtual Machine-Netzwerk ab und speichert ihn dann in der $NetworkMapping-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e0913-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="e0913-119">Der Befehl gibt den primären Server für das Netzwerk als erstes Element $Servers an.</span><span class="sxs-lookup"><span data-stu-id="e0913-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="e0913-120">Der Befehl gibt den *Azure* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="e0913-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="e0913-121">Daher ruft der Befehl die Zuordnung zu einem Azure Virtual Machine-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="e0913-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="e0913-122">Der endgültige Befehl entfernt die Netzwerkzuordnung in $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="e0913-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="e0913-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0913-123">PARAMETERS</span></span>

### <span data-ttu-id="e0913-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e0913-124">-NetworkMapping</span></span>
<span data-ttu-id="e0913-125">Gibt die zu entfernende Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="e0913-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0913-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0913-126">-Profile</span></span>
<span data-ttu-id="e0913-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e0913-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0913-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e0913-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0913-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0913-129">CommonParameters</span></span>
<span data-ttu-id="e0913-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0913-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0913-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0913-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0913-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0913-132">INPUTS</span></span>

## <span data-ttu-id="e0913-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0913-133">OUTPUTS</span></span>

## <span data-ttu-id="e0913-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0913-134">NOTES</span></span>

## <span data-ttu-id="e0913-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0913-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0913-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e0913-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="e0913-137">Neu – AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e0913-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="e0913-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e0913-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


