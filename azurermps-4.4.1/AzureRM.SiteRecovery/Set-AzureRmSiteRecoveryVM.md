---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 7cfc764e5c9c3c5bb11290220cc04b2baa781070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500677"
---
# <span data-ttu-id="c3b7a-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="c3b7a-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="c3b7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b7a-103">Legt die Wiederherstellungs seitigen Optionen für eine Website Wiederherstellungs Schutz Entität fest.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3b7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3b7a-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3b7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3b7a-105">DESCRIPTION</span></span>
<span data-ttu-id="c3b7a-106">Das Cmdlet " **Set-AzureRmSiteRecoveryVM** " legt die Optionen für den Wiederherstellungs seitigen Schutz fest, beispielsweise die Größe der Wiederherstellungs-und Wiederherstellungs-Virtual Machine-Netzwerk für Azure Site Recovery Protection-Entitäten.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="c3b7a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3b7a-107">EXAMPLES</span></span>

## <span data-ttu-id="c3b7a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3b7a-108">PARAMETERS</span></span>

### <span data-ttu-id="c3b7a-109">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b7a-109">-Name</span></span>
<span data-ttu-id="c3b7a-110">Gibt den Namen der virtuellen Zielmaschine an.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-110">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="c3b7a-111">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="c3b7a-111">-NicSelectionType</span></span>
<span data-ttu-id="c3b7a-112">Gibt die Auswahl Eigenschaften des Netzwerkadapters an.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-112">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="c3b7a-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3b7a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3b7a-114">NotSelected</span><span class="sxs-lookup"><span data-stu-id="c3b7a-114">NotSelected</span></span>
- <span data-ttu-id="c3b7a-115">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="c3b7a-115">SelectedByUser</span></span>

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

### <span data-ttu-id="c3b7a-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="c3b7a-116">-PrimaryNic</span></span>
<span data-ttu-id="c3b7a-117">Gibt die primäre Netzwerkadapterkarte an.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-117">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="c3b7a-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="c3b7a-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="c3b7a-119">Gibt die Wiederherstellungs Netzwerk-ID an.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-119">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="c3b7a-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="c3b7a-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="c3b7a-121">Gibt die statische IP-Adresse an, die dem primären Netzwerkadapter Controller bei der Wiederherstellung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-121">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="c3b7a-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c3b7a-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="c3b7a-123">Gibt den Namen des Azure Virtual Network-Subnetzes an, mit dem der primäre Netzwerkadapter-Controller bei der Wiederherstellung angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-123">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="c3b7a-124">-Size</span><span class="sxs-lookup"><span data-stu-id="c3b7a-124">-Size</span></span>
<span data-ttu-id="c3b7a-125">Gibt die Größe des virtuellen Zielcomputers an.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-125">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="c3b7a-126">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c3b7a-126">-VirtualMachine</span></span>
<span data-ttu-id="c3b7a-127">Gibt das Objekt für den virtuellen Computer der Websitewiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-127">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b7a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b7a-128">-DefaultProfile</span></span>
<span data-ttu-id="c3b7a-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3b7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b7a-130">CommonParameters</span></span>
<span data-ttu-id="c3b7a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b7a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b7a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b7a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3b7a-133">INPUTS</span></span>

### <span data-ttu-id="c3b7a-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c3b7a-134">ASRVirtualMachine</span></span>
<span data-ttu-id="c3b7a-135">Der Parameter "VirtualMachine" akzeptiert den Wert vom Typ "ASRVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3b7a-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="c3b7a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3b7a-136">OUTPUTS</span></span>

### <span data-ttu-id="c3b7a-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c3b7a-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c3b7a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3b7a-138">NOTES</span></span>

## <span data-ttu-id="c3b7a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3b7a-139">RELATED LINKS</span></span>

[<span data-ttu-id="c3b7a-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="c3b7a-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
