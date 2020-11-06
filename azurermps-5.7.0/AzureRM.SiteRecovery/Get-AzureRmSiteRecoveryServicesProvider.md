---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502401"
---
# <span data-ttu-id="cc773-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="cc773-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="cc773-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc773-102">SYNOPSIS</span></span>
<span data-ttu-id="cc773-103">Ruft Informationen zu den Azure Site Recovery-Anbietern im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="cc773-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc773-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc773-104">SYNTAX</span></span>

### <span data-ttu-id="cc773-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc773-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc773-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cc773-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc773-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cc773-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc773-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc773-108">DESCRIPTION</span></span>
<span data-ttu-id="cc773-109">Das Cmdlet " **Get-AzureRmSiteRecoveryServicesProvider** " Ruft Informationen zu den Azure Site Recovery-Anbietern im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="cc773-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="cc773-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc773-110">EXAMPLES</span></span>

## <span data-ttu-id="cc773-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc773-111">PARAMETERS</span></span>

### <span data-ttu-id="cc773-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc773-112">-DefaultProfile</span></span>
<span data-ttu-id="cc773-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc773-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc773-114">-Stoff</span><span class="sxs-lookup"><span data-stu-id="cc773-114">-Fabric</span></span>
<span data-ttu-id="cc773-115">Gibt das Fabric-Objekt für Azure Site Recovery an.</span><span class="sxs-lookup"><span data-stu-id="cc773-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc773-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cc773-116">-FriendlyName</span></span>
<span data-ttu-id="cc773-117">Gibt den Anzeigenamen des Azure Site Recovery-Anbieters an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cc773-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc773-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cc773-118">-Name</span></span>
<span data-ttu-id="cc773-119">Gibt den Namen des Azure Site Recovery Providers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cc773-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc773-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc773-120">CommonParameters</span></span>
<span data-ttu-id="cc773-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc773-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc773-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc773-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc773-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc773-123">INPUTS</span></span>

### <span data-ttu-id="cc773-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cc773-124">ASRFabric</span></span>
<span data-ttu-id="cc773-125">Der Parameter "Fabric" akzeptiert den Wert vom Typ "ASRFabric" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc773-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="cc773-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc773-126">OUTPUTS</span></span>

### <span data-ttu-id="cc773-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cc773-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cc773-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc773-128">NOTES</span></span>

## <span data-ttu-id="cc773-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc773-129">RELATED LINKS</span></span>

[<span data-ttu-id="cc773-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="cc773-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="cc773-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="cc773-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
