---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: 2595d8feaa01c2f3ccd9f16ca193be195a8e303a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503938"
---
# <span data-ttu-id="67767-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="67767-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="67767-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67767-102">SYNOPSIS</span></span>
<span data-ttu-id="67767-103">Ruft Schutzcontainer für das aktuelle Standort Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="67767-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67767-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67767-104">SYNTAX</span></span>

### <span data-ttu-id="67767-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="67767-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67767-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="67767-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67767-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="67767-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67767-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="67767-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67767-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="67767-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67767-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="67767-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67767-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67767-111">DESCRIPTION</span></span>
<span data-ttu-id="67767-112">Das Cmdlet " **Get-AzureRmSiteRecoveryProtectionContainer** " erhält Schutzcontainer für das aktuelle Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="67767-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="67767-113">Ein Schutzcontainer ist ein logischer Container für geschützte Objekte wie virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="67767-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="67767-114">Schutzrichtlinien definieren Replikationseinstellungen für geschützte Elemente und können einem Schutzcontainer zugeordnet und auf eine geschützte Entität angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="67767-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="67767-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67767-115">EXAMPLES</span></span>

## <span data-ttu-id="67767-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="67767-116">PARAMETERS</span></span>

### <span data-ttu-id="67767-117">-Stoff</span><span class="sxs-lookup"><span data-stu-id="67767-117">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67767-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="67767-118">-FriendlyName</span></span>
<span data-ttu-id="67767-119">Gibt den Anzeigenamen des Schutz Containers an.</span><span class="sxs-lookup"><span data-stu-id="67767-119">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67767-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67767-120">-Name</span></span>
<span data-ttu-id="67767-121">Gibt den Namen des Schutz Containers an.</span><span class="sxs-lookup"><span data-stu-id="67767-121">Specifies the name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67767-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67767-122">-DefaultProfile</span></span>
<span data-ttu-id="67767-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67767-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67767-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67767-124">CommonParameters</span></span>
<span data-ttu-id="67767-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67767-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67767-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67767-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67767-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67767-127">INPUTS</span></span>

### <span data-ttu-id="67767-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="67767-128">ASRFabric</span></span>
<span data-ttu-id="67767-129">Der Parameter "Fabric" akzeptiert den Wert vom Typ "ASRFabric" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="67767-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="67767-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67767-130">OUTPUTS</span></span>

### <span data-ttu-id="67767-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="67767-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="67767-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="67767-132">NOTES</span></span>

## <span data-ttu-id="67767-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67767-133">RELATED LINKS</span></span>

