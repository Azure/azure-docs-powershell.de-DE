---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 477f31ea84c5cb3e9c06b79e1ae70f5ae8a93925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501602"
---
# <span data-ttu-id="68ea1-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="68ea1-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="68ea1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="68ea1-103">Startet einen Standort Wiederherstellungs-Replikationsrichtlinien Zuordnungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="68ea1-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68ea1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ea1-104">SYNTAX</span></span>

### <span data-ttu-id="68ea1-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="68ea1-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68ea1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="68ea1-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68ea1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68ea1-107">DESCRIPTION</span></span>
<span data-ttu-id="68ea1-108">Das Cmdlet **Start-AzureRmSiteRecoveryPolicyAssociationJob** initiiert einen Zuordnungs Auftrag, um eine Replikationsrichtlinie einem Azure Site Recovery Protection-Container zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="68ea1-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="68ea1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68ea1-109">EXAMPLES</span></span>

## <span data-ttu-id="68ea1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ea1-110">PARAMETERS</span></span>

### <span data-ttu-id="68ea1-111">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="68ea1-111">-Policy</span></span>
<span data-ttu-id="68ea1-112">Gibt das Website Wiederherstellungsrichtlinien Objekt an.</span><span class="sxs-lookup"><span data-stu-id="68ea1-112">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="68ea1-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="68ea1-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="68ea1-114">Gibt den primären Schutzcontainer an, auf dem die Schutzprofil Einstellungen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68ea1-114">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="68ea1-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="68ea1-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="68ea1-116">Gibt den Wiederherstellungs Schutzcontainer an, auf dem die Schutzprofil Einstellungen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68ea1-116">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="68ea1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ea1-117">-DefaultProfile</span></span>
<span data-ttu-id="68ea1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68ea1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ea1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ea1-119">CommonParameters</span></span>
<span data-ttu-id="68ea1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ea1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ea1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ea1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ea1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68ea1-122">INPUTS</span></span>

### <span data-ttu-id="68ea1-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="68ea1-123">ASRPolicy</span></span>
<span data-ttu-id="68ea1-124">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="68ea1-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="68ea1-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68ea1-125">OUTPUTS</span></span>

### <span data-ttu-id="68ea1-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68ea1-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68ea1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="68ea1-127">NOTES</span></span>

## <span data-ttu-id="68ea1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68ea1-128">RELATED LINKS</span></span>

