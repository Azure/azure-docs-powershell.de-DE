---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481489"
---
# <span data-ttu-id="29397-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="29397-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="29397-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29397-102">SYNOPSIS</span></span>
<span data-ttu-id="29397-103">Startet einen Dissoziation-Auftrag für eine Replikationsrichtlinie, die einem Schutzcontainer für die Standortwiederherstellung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="29397-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29397-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29397-104">SYNTAX</span></span>

### <span data-ttu-id="29397-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="29397-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29397-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="29397-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29397-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29397-107">DESCRIPTION</span></span>
<span data-ttu-id="29397-108">Das Cmdlet **Start-AzureRmSiteRecoveryPolicyDissociationJob** initiiert einen Dissoziation-Auftrag in der Replikationsrichtlinie, die einem Azure Site Recovery Protection-Container zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="29397-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="29397-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29397-109">EXAMPLES</span></span>

## <span data-ttu-id="29397-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29397-110">PARAMETERS</span></span>

### <span data-ttu-id="29397-111">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="29397-111">-Policy</span></span>
<span data-ttu-id="29397-112">Gibt ein Azure Site Recovery Policy-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="29397-112">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29397-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="29397-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="29397-114">Gibt einen primären Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="29397-114">Specifies a primary protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29397-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="29397-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="29397-116">Gibt einen Wiederherstellungs Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="29397-116">Specifies a recovery protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29397-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29397-117">-DefaultProfile</span></span>
<span data-ttu-id="29397-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29397-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29397-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29397-119">CommonParameters</span></span>
<span data-ttu-id="29397-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29397-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29397-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29397-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29397-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29397-122">INPUTS</span></span>

### <span data-ttu-id="29397-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="29397-123">ASRPolicy</span></span>
<span data-ttu-id="29397-124">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="29397-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="29397-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29397-125">OUTPUTS</span></span>

### <span data-ttu-id="29397-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="29397-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29397-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="29397-127">NOTES</span></span>

## <span data-ttu-id="29397-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29397-128">RELATED LINKS</span></span>

