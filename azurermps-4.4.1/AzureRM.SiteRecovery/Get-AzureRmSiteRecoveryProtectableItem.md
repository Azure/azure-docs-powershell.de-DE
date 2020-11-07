---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 0b2fe8f500e17bc21407870a712ad4b9f00fd544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662606"
---
# <span data-ttu-id="a345d-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a345d-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="a345d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a345d-102">SYNOPSIS</span></span>
<span data-ttu-id="a345d-103">Rufen Sie die geschützten Elemente in einem Schutz Container ab.</span><span class="sxs-lookup"><span data-stu-id="a345d-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a345d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a345d-104">SYNTAX</span></span>

### <span data-ttu-id="a345d-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="a345d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a345d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a345d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a345d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a345d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a345d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a345d-108">DESCRIPTION</span></span>
<span data-ttu-id="a345d-109">Das Cmdlet " **Get-AzureRmSiteRecoveryProtectableItem** " Ruft die geschützten Elemente in einem Azure Site Recovery Protection-Container ab.</span><span class="sxs-lookup"><span data-stu-id="a345d-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="a345d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a345d-110">EXAMPLES</span></span>

## <span data-ttu-id="a345d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a345d-111">PARAMETERS</span></span>

### <span data-ttu-id="a345d-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a345d-112">-FriendlyName</span></span>
<span data-ttu-id="a345d-113">Gibt den Anzeigenamen des geschützten Elements Azure Site Recovery an.</span><span class="sxs-lookup"><span data-stu-id="a345d-113">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a345d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a345d-114">-Name</span></span>
<span data-ttu-id="a345d-115">Gibt den Namen des geschützten Elements Azure Site Recovery an.</span><span class="sxs-lookup"><span data-stu-id="a345d-115">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a345d-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a345d-116">-ProtectionContainer</span></span>
<span data-ttu-id="a345d-117">Gibt das Azure Site Recovery Protection-Container Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a345d-117">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a345d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a345d-118">-DefaultProfile</span></span>
<span data-ttu-id="a345d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a345d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a345d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a345d-120">CommonParameters</span></span>
<span data-ttu-id="a345d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a345d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a345d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a345d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a345d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a345d-123">INPUTS</span></span>

### <span data-ttu-id="a345d-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a345d-124">ASRProtectionContainer</span></span>
<span data-ttu-id="a345d-125">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a345d-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="a345d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a345d-126">OUTPUTS</span></span>

### <span data-ttu-id="a345d-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a345d-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a345d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a345d-128">NOTES</span></span>

## <span data-ttu-id="a345d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a345d-129">RELATED LINKS</span></span>

[<span data-ttu-id="a345d-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a345d-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="a345d-131">Satz-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a345d-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
