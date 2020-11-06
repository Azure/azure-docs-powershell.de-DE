---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 869b22c881652680be31c541c6d70d95a45be43d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481518"
---
# <span data-ttu-id="d03ec-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d03ec-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d03ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d03ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d03ec-103">Ruft Azure Site Recovery Protection-Container Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="d03ec-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d03ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d03ec-104">SYNTAX</span></span>

### <span data-ttu-id="d03ec-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="d03ec-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d03ec-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d03ec-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d03ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d03ec-107">DESCRIPTION</span></span>
<span data-ttu-id="d03ec-108">Das Cmdlet " **Get-AzureRmSiteRecoveryProtectionContainerMapping** " Ruft Informationen über den Schutz Container für Richtlinienzuordnungen im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="d03ec-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="d03ec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d03ec-109">EXAMPLES</span></span>

## <span data-ttu-id="d03ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d03ec-110">PARAMETERS</span></span>

### <span data-ttu-id="d03ec-111">-Name</span><span class="sxs-lookup"><span data-stu-id="d03ec-111">-Name</span></span>
<span data-ttu-id="d03ec-112">Gibt den Namen der Schutz Container Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="d03ec-112">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="d03ec-113">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d03ec-113">-ProtectionContainer</span></span>
<span data-ttu-id="d03ec-114">Gibt das Azure Site Recovery Protection-Container Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d03ec-114">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="d03ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03ec-115">-DefaultProfile</span></span>
<span data-ttu-id="d03ec-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d03ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d03ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03ec-117">CommonParameters</span></span>
<span data-ttu-id="d03ec-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d03ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03ec-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03ec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03ec-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d03ec-120">INPUTS</span></span>

### <span data-ttu-id="d03ec-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d03ec-121">ASRProtectionContainer</span></span>
<span data-ttu-id="d03ec-122">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d03ec-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="d03ec-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d03ec-123">OUTPUTS</span></span>

### <span data-ttu-id="d03ec-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d03ec-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d03ec-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d03ec-125">NOTES</span></span>

## <span data-ttu-id="d03ec-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d03ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="d03ec-127">Neu – AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d03ec-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d03ec-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d03ec-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
