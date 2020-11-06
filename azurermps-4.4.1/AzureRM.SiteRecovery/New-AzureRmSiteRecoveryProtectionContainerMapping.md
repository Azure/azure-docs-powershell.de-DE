---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500690"
---
# <span data-ttu-id="8879c-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8879c-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="8879c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8879c-102">SYNOPSIS</span></span>
<span data-ttu-id="8879c-103">Erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem eine Richtlinie einem Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="8879c-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8879c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8879c-104">SYNTAX</span></span>

### <span data-ttu-id="8879c-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="8879c-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8879c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8879c-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8879c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8879c-107">DESCRIPTION</span></span>
<span data-ttu-id="8879c-108">Das Cmdlet **New-AzureRmSiteRecoveryProtectionContainerMapping** erstellt eine Azure Site Recovery Protection-Container Zuordnung, indem eine Richtlinie einem Schutzcontainer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="8879c-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="8879c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8879c-109">EXAMPLES</span></span>

## <span data-ttu-id="8879c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8879c-110">PARAMETERS</span></span>

### <span data-ttu-id="8879c-111">-Name</span><span class="sxs-lookup"><span data-stu-id="8879c-111">-Name</span></span>
<span data-ttu-id="8879c-112">Gibt den Namen der Schutz Container Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="8879c-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8879c-113">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="8879c-113">-Policy</span></span>
<span data-ttu-id="8879c-114">Gibt das Azure-Website Wiederherstellungsrichtlinien Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8879c-114">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="8879c-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8879c-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="8879c-116">Gibt das primäre Schutz Container Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8879c-116">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="8879c-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8879c-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="8879c-118">Gibt das Container Objekt für den Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="8879c-118">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="8879c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8879c-119">-DefaultProfile</span></span>
<span data-ttu-id="8879c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8879c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8879c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8879c-121">CommonParameters</span></span>
<span data-ttu-id="8879c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8879c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8879c-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8879c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8879c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8879c-124">INPUTS</span></span>

### <span data-ttu-id="8879c-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8879c-125">ASRPolicy</span></span>
<span data-ttu-id="8879c-126">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8879c-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="8879c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8879c-127">OUTPUTS</span></span>

### <span data-ttu-id="8879c-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8879c-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8879c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8879c-129">NOTES</span></span>

## <span data-ttu-id="8879c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8879c-130">RELATED LINKS</span></span>

[<span data-ttu-id="8879c-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8879c-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="8879c-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8879c-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
