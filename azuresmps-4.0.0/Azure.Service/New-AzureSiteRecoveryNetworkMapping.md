---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006423"
---
# <span data-ttu-id="d4cc0-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d4cc0-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="d4cc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cc0-103">Erstellt eine Zuordnung zwischen virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="d4cc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4cc0-104">SYNTAX</span></span>

### <span data-ttu-id="d4cc0-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d4cc0-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d4cc0-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d4cc0-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4cc0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4cc0-107">DESCRIPTION</span></span>
<span data-ttu-id="d4cc0-108">Mit dem Cmdlet **New-AzureSiteRecoveryNetworkMapping** wird eine Zuordnung zwischen zwei virtuellen Netzwerken erstellt, und es wird ein Azure Site Recovery-Auftrag zurückgegeben, um ihn zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="d4cc0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4cc0-109">EXAMPLES</span></span>

### <span data-ttu-id="d4cc0-110">Beispiel 1: Erstellen einer Zuordnung zwischen einem Netzwerk und einem Wiederherstellungs Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d4cc0-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="d4cc0-111">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="d4cc0-112">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="d4cc0-113">Der zweite Befehl ruft das Standort Wiederherstellungs Netzwerk für den ersten Server im $Servers-Array mit dem Cmdlet **Get-AzureSiteRecoveryNetwork** ab.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="d4cc0-114">Der Befehl speichert die Netzwerke in der $Networks-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="d4cc0-115">Der endgültige Befehl erstellt eine Zuordnung zwischen dem primären Netzwerk und dem Wiederherstellungs Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="d4cc0-116">Der Befehl gibt das primäre Netzwerk als erstes Element von $Networks an.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="d4cc0-117">Der Befehl gibt das Wiederherstellungs Netzwerk als zweites Element von $Networks an.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="d4cc0-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4cc0-118">PARAMETERS</span></span>

### <span data-ttu-id="d4cc0-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4cc0-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="d4cc0-120">Gibt die ID Ihres Azure-Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-120">Specifies the ID of your Azure subscription.</span></span>

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

### <span data-ttu-id="d4cc0-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d4cc0-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="d4cc0-122">Gibt die Azure Virtual Network-ID an.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-122">Specifies the Azure virtual network ID.</span></span>

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

### <span data-ttu-id="d4cc0-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="d4cc0-123">-PrimaryNetwork</span></span>
<span data-ttu-id="d4cc0-124">Gibt das primäre Netzwerkobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cc0-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d4cc0-125">-Profile</span></span>
<span data-ttu-id="d4cc0-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4cc0-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4cc0-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d4cc0-128">-RecoveryNetwork</span></span>
<span data-ttu-id="d4cc0-129">Gibt das Wiederherstellungs Netzwerkobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cc0-130">CommonParameters</span></span>
<span data-ttu-id="d4cc0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cc0-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4cc0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cc0-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4cc0-133">INPUTS</span></span>

## <span data-ttu-id="d4cc0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4cc0-134">OUTPUTS</span></span>

## <span data-ttu-id="d4cc0-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4cc0-135">NOTES</span></span>

## <span data-ttu-id="d4cc0-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4cc0-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4cc0-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d4cc0-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="d4cc0-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d4cc0-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="d4cc0-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d4cc0-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


