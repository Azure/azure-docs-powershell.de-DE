---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481506"
---
# <span data-ttu-id="c98b2-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c98b2-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="c98b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c98b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c98b2-103">Legt Wiederherstellungseigenschaften wie das Zielnetzwerk und die Größe des virtuellen Computers für ein geschütztes Replikations Element fest.</span><span class="sxs-lookup"><span data-stu-id="c98b2-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c98b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c98b2-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c98b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c98b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c98b2-106">Das Cmdlet " **Set-AzureRmSiteRecoveryReplicationProtectedItem** " legt die Wiederherstellungseigenschaften für ein geschütztes Replikations Element fest.</span><span class="sxs-lookup"><span data-stu-id="c98b2-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="c98b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c98b2-107">EXAMPLES</span></span>

## <span data-ttu-id="c98b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c98b2-108">PARAMETERS</span></span>

### <span data-ttu-id="c98b2-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c98b2-109">-LicenseType</span></span>
<span data-ttu-id="c98b2-110">Gibt die Auswahl des Lizenztyps für virtuelle Windows Server-Computer an, die über die Hybrid Nutzung Benefit migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c98b2-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-111">-Name</span><span class="sxs-lookup"><span data-stu-id="c98b2-111">-Name</span></span>
<span data-ttu-id="c98b2-112">Gibt den Namen der virtuellen Wiederherstellungs Maschine an.</span><span class="sxs-lookup"><span data-stu-id="c98b2-112">Specifies the name of the recovery virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="c98b2-113">-NicSelectionType</span></span>
<span data-ttu-id="c98b2-114">Gibt die Netzwerkschnittstellenkarten Eigenschaften (NIC) an, die standardmäßig vom Benutzer festgelegt oder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c98b2-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="c98b2-115">Sie können NotSelected angeben, um zu den Standardwerten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="c98b2-115">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="c98b2-116">-PrimaryNic</span></span>
<span data-ttu-id="c98b2-117">Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet die Wiederherstellungs Netzwerk Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="c98b2-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="c98b2-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="c98b2-119">Gibt die ID des virtuellen Azure-Netzwerks an, für das mit diesem Cmdlet das geschützte Element erneut hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c98b2-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="c98b2-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="c98b2-121">Gibt die statische IP-Adresse an, die der primären NIC bei der Wiederherstellung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c98b2-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c98b2-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="c98b2-123">Gibt den Namen des Subnets im virtuellen Recovery Azure-Netzwerk an, für das dieses Cmdlet das geschützte Element wiederhergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="c98b2-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c98b2-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c98b2-125">Gibt das geschütztes Element der Azure Site Recovery-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="c98b2-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-126">-Size</span><span class="sxs-lookup"><span data-stu-id="c98b2-126">-Size</span></span>
<span data-ttu-id="c98b2-127">Gibt die Größe der virtuellen Wiederherstellungs Maschine an.</span><span class="sxs-lookup"><span data-stu-id="c98b2-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="c98b2-128">Der Wert sollte aus den von Azure Virtual Machines unterstützten Größen Sätzen sein.</span><span class="sxs-lookup"><span data-stu-id="c98b2-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98b2-129">-DefaultProfile</span></span>
<span data-ttu-id="c98b2-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c98b2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98b2-131">CommonParameters</span></span>
<span data-ttu-id="c98b2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98b2-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98b2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98b2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c98b2-134">INPUTS</span></span>

### <span data-ttu-id="c98b2-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c98b2-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c98b2-136">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c98b2-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c98b2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c98b2-137">OUTPUTS</span></span>

### <span data-ttu-id="c98b2-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c98b2-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c98b2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c98b2-139">NOTES</span></span>

## <span data-ttu-id="c98b2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c98b2-140">RELATED LINKS</span></span>

[<span data-ttu-id="c98b2-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c98b2-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c98b2-142">Neu – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c98b2-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c98b2-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c98b2-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
