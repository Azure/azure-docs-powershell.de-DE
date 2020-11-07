---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664186"
---
# <span data-ttu-id="4c0b6-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c0b6-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="4c0b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0b6-103">Ruft die Eigenschaften von geschützten Azure Site Recovery-Elementen ab.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c0b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c0b6-104">SYNTAX</span></span>

### <span data-ttu-id="4c0b6-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c0b6-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0b6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4c0b6-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0b6-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c0b6-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0b6-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="4c0b6-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c0b6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c0b6-109">DESCRIPTION</span></span>
<span data-ttu-id="4c0b6-110">Das Cmdlet " **Get-AzureRmSiteRecoveryReplicationProtectedItem** " Ruft die Eigenschaften von geschützten Azure Site Recovery-Elementen ab.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="4c0b6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c0b6-111">EXAMPLES</span></span>

## <span data-ttu-id="4c0b6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c0b6-112">PARAMETERS</span></span>

### <span data-ttu-id="4c0b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0b6-113">-DefaultProfile</span></span>
<span data-ttu-id="4c0b6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c0b6-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c0b6-115">-FriendlyName</span></span>
<span data-ttu-id="4c0b6-116">Gibt den Anzeigenamen des vom Cmdlet abgerufenen Replikations geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4c0b6-117">-Name</span></span>
<span data-ttu-id="4c0b6-118">Gibt den Namen des Replikations geschützten Elements an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b6-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4c0b6-119">-ProtectableItem</span></span>
<span data-ttu-id="4c0b6-120">Gibt das zu schützende Element an, das dem Replikations geschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b6-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4c0b6-121">-ProtectionContainer</span></span>
<span data-ttu-id="4c0b6-122">Gibt das Azure Site Recovery Protection-Container Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0b6-123">CommonParameters</span></span>
<span data-ttu-id="4c0b6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0b6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0b6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0b6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c0b6-126">INPUTS</span></span>

### <span data-ttu-id="4c0b6-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4c0b6-127">ASRProtectableItem</span></span>
<span data-ttu-id="4c0b6-128">Der Parameter "ProtectableItem" akzeptiert den Wert vom Typ "ASRProtectableItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="4c0b6-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4c0b6-129">ASRProtectionContainer</span></span>
<span data-ttu-id="4c0b6-130">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c0b6-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="4c0b6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c0b6-131">OUTPUTS</span></span>

### <span data-ttu-id="4c0b6-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4c0b6-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4c0b6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c0b6-133">NOTES</span></span>

## <span data-ttu-id="4c0b6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c0b6-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c0b6-135">Neu – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c0b6-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="4c0b6-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c0b6-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="4c0b6-137">Satz-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c0b6-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
