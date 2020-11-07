---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 36f5c6e535cc67029fac7c951cbc6dbbe3c73091
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664175"
---
# <span data-ttu-id="c2429-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2429-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="c2429-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2429-102">SYNOPSIS</span></span>
<span data-ttu-id="c2429-103">Erstellt eine Zuordnung zwischen virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="c2429-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2429-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2429-104">SYNTAX</span></span>

### <span data-ttu-id="c2429-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c2429-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2429-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c2429-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2429-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2429-107">DESCRIPTION</span></span>
<span data-ttu-id="c2429-108">Mit dem Cmdlet **New-AzureRMSiteRecoveryNetworkMapping** wird eine Zuordnung zwischen zwei virtuellen Netzwerken erstellt, und es wird ein Azure Site Recovery-Auftrag zurückgegeben, um ihn zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c2429-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="c2429-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2429-109">EXAMPLES</span></span>

## <span data-ttu-id="c2429-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2429-110">PARAMETERS</span></span>

### <span data-ttu-id="c2429-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c2429-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="c2429-112">Gibt die Azure Virtual Network-ID an.</span><span class="sxs-lookup"><span data-stu-id="c2429-112">Specifies the Azure virtual network ID.</span></span>

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

### <span data-ttu-id="c2429-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2429-113">-DefaultProfile</span></span>
<span data-ttu-id="c2429-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2429-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2429-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c2429-115">-Name</span></span>
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

### <span data-ttu-id="c2429-116">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c2429-116">-PrimaryNetwork</span></span>
<span data-ttu-id="c2429-117">Gibt das primäre Netzwerkobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c2429-117">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2429-118">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c2429-118">-RecoveryNetwork</span></span>
<span data-ttu-id="c2429-119">Gibt das Wiederherstellungs Netzwerkobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c2429-119">Specifies the recovery network object.</span></span>

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

### <span data-ttu-id="c2429-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2429-120">CommonParameters</span></span>
<span data-ttu-id="c2429-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2429-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2429-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2429-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2429-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2429-123">INPUTS</span></span>

### <span data-ttu-id="c2429-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c2429-124">ASRNetwork</span></span>
<span data-ttu-id="c2429-125">Der Parameter "PrimaryNetwork" akzeptiert den Wert vom Typ "ASRNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2429-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="c2429-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2429-126">OUTPUTS</span></span>

### <span data-ttu-id="c2429-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c2429-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c2429-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2429-128">NOTES</span></span>

## <span data-ttu-id="c2429-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2429-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2429-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2429-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="c2429-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2429-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
