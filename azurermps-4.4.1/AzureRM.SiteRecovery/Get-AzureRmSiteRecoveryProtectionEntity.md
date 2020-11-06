---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504725"
---
# <span data-ttu-id="42e87-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="42e87-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="42e87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42e87-102">SYNOPSIS</span></span>
<span data-ttu-id="42e87-103">Ruft eine Liste geschützter oder geschützter Entitäten im aktuellen Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="42e87-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42e87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42e87-104">SYNTAX</span></span>

### <span data-ttu-id="42e87-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="42e87-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e87-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="42e87-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e87-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="42e87-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e87-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42e87-108">DESCRIPTION</span></span>
<span data-ttu-id="42e87-109">Das Cmdlet " **Get-AzureRmSiteRecoveryProtectionEntity** " ruft im aktuellen Azure Site Recovery Vault eine Liste mit schützenden oder geschützten Entitäten wie virtuellen Computern ab.</span><span class="sxs-lookup"><span data-stu-id="42e87-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="42e87-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42e87-110">EXAMPLES</span></span>

## <span data-ttu-id="42e87-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="42e87-111">PARAMETERS</span></span>

### <span data-ttu-id="42e87-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="42e87-112">-FriendlyName</span></span>
<span data-ttu-id="42e87-113">Gibt den Anzeigenamen der Schutz Entität an.</span><span class="sxs-lookup"><span data-stu-id="42e87-113">Specifies the friendly name of the protection entity.</span></span>

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

### <span data-ttu-id="42e87-114">-Name</span><span class="sxs-lookup"><span data-stu-id="42e87-114">-Name</span></span>
<span data-ttu-id="42e87-115">Gibt den Namen der Schutz Entität an.</span><span class="sxs-lookup"><span data-stu-id="42e87-115">Specifies the name of the protection entity.</span></span>

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

### <span data-ttu-id="42e87-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="42e87-116">-ProtectionContainer</span></span>
<span data-ttu-id="42e87-117">Gibt das Schutzcontainer Objekt an.</span><span class="sxs-lookup"><span data-stu-id="42e87-117">Specifies the protection container object.</span></span>

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

### <span data-ttu-id="42e87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e87-118">-DefaultProfile</span></span>
<span data-ttu-id="42e87-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42e87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e87-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e87-120">CommonParameters</span></span>
<span data-ttu-id="42e87-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e87-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e87-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e87-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e87-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42e87-123">INPUTS</span></span>

### <span data-ttu-id="42e87-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="42e87-124">ASRProtectionContainer</span></span>
<span data-ttu-id="42e87-125">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="42e87-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="42e87-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42e87-126">OUTPUTS</span></span>

### <span data-ttu-id="42e87-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="42e87-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="42e87-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="42e87-128">NOTES</span></span>

## <span data-ttu-id="42e87-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42e87-129">RELATED LINKS</span></span>

[<span data-ttu-id="42e87-130">Satz-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="42e87-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
