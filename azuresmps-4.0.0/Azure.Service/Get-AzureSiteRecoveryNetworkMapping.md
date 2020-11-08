---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005796"
---
# <span data-ttu-id="3497b-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3497b-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="3497b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3497b-102">SYNOPSIS</span></span>
<span data-ttu-id="3497b-103">Ruft Netzwerkzuordnungen für ein Website Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="3497b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3497b-104">SYNTAX</span></span>

### <span data-ttu-id="3497b-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3497b-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3497b-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="3497b-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3497b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3497b-107">DESCRIPTION</span></span>
<span data-ttu-id="3497b-108">Das Cmdlet " **Get-AzureSiteRecoveryNetworkMapping** " Ruft Informationen zu Azure Site Recovery-Netzwerkzuordnungen für das aktuelle Standort Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="3497b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3497b-109">EXAMPLES</span></span>

### <span data-ttu-id="3497b-110">Beispiel 1: Abrufen der Zuordnung zwischen einem Netzwerk und einem Wiederherstellungs Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3497b-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="3497b-111">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="3497b-112">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="3497b-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="3497b-113">Der zweite Befehl ruft die Zuordnung zwischen dem primären Netzwerk und dem Wiederherstellungs Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="3497b-114">Der Befehl gibt den primären Server für die Netzwerkzuordnung als erstes Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="3497b-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="3497b-115">Der Befehl gibt den Server für das Wiederherstellungs Netzwerk als zweites Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="3497b-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="3497b-116">Beispiel 2: Abrufen der Zuordnung zwischen einem Netzwerk und einem Azure Virtual Machine-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3497b-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="3497b-117">Das Cmdlet "erster Befehl" Ruft Server für den aktuellen Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="3497b-118">Der Befehl speichert die Server in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="3497b-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="3497b-119">Der zweite Befehl ruft eine Zuordnung zwischen dem primären Netzwerk und einem Azure Virtual Machine-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="3497b-120">Der Befehl gibt den primären Server für das Netzwerk als erstes Element $Servers an.</span><span class="sxs-lookup"><span data-stu-id="3497b-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="3497b-121">Der Befehl gibt den *Azure* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="3497b-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="3497b-122">Daher ruft der Befehl die Zuordnung zu einem Azure Virtual Machine-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="3497b-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="3497b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="3497b-123">PARAMETERS</span></span>

### <span data-ttu-id="3497b-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="3497b-124">-Azure</span></span>
<span data-ttu-id="3497b-125">Gibt an, dass dieses Cmdlet Netzwerkzuordnungen für Netzwerke auf dem primären Server erhält, die Azure virtuellen Netzwerken zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3497b-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3497b-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="3497b-126">-PrimaryServer</span></span>
<span data-ttu-id="3497b-127">Gibt einen primären Server an, für den Zuordnungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3497b-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3497b-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="3497b-128">-Profile</span></span>
<span data-ttu-id="3497b-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3497b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3497b-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3497b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3497b-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="3497b-131">-RecoveryServer</span></span>
<span data-ttu-id="3497b-132">Gibt einen Wiederherstellungsserver an, für den Zuordnungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3497b-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3497b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3497b-133">CommonParameters</span></span>
<span data-ttu-id="3497b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3497b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3497b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3497b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3497b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3497b-136">INPUTS</span></span>

## <span data-ttu-id="3497b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3497b-137">OUTPUTS</span></span>

## <span data-ttu-id="3497b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3497b-138">NOTES</span></span>

## <span data-ttu-id="3497b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3497b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3497b-140">Neu – AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3497b-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="3497b-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3497b-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


