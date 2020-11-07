---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664717"
---
# <span data-ttu-id="64a6c-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="64a6c-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="64a6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="64a6c-103">Erstellt eine Azure Website-Wiederherstellungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="64a6c-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64a6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a6c-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64a6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64a6c-105">DESCRIPTION</span></span>
<span data-ttu-id="64a6c-106">Das Cmdlet **New-AzureRmSiteRecoveryFabric** erstellt ein Azure Site Recovery-Fabric des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="64a6c-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="64a6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a6c-107">EXAMPLES</span></span>

## <span data-ttu-id="64a6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="64a6c-108">PARAMETERS</span></span>

### <span data-ttu-id="64a6c-109">-Name</span><span class="sxs-lookup"><span data-stu-id="64a6c-109">-Name</span></span>
<span data-ttu-id="64a6c-110">Gibt den Namen des Azure Site Recovery-Fabrics an.</span><span class="sxs-lookup"><span data-stu-id="64a6c-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="64a6c-111">-Typ</span><span class="sxs-lookup"><span data-stu-id="64a6c-111">-Type</span></span>
<span data-ttu-id="64a6c-112">Gibt den Fabric-Typ "Azure Site Recovery" an.</span><span class="sxs-lookup"><span data-stu-id="64a6c-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a6c-113">-DefaultProfile</span></span>
<span data-ttu-id="64a6c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64a6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64a6c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a6c-115">CommonParameters</span></span>
<span data-ttu-id="64a6c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a6c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a6c-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64a6c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a6c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64a6c-118">INPUTS</span></span>

## <span data-ttu-id="64a6c-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64a6c-119">OUTPUTS</span></span>

### <span data-ttu-id="64a6c-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="64a6c-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64a6c-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="64a6c-121">NOTES</span></span>

## <span data-ttu-id="64a6c-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64a6c-122">RELATED LINKS</span></span>

[<span data-ttu-id="64a6c-123">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="64a6c-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="64a6c-124">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="64a6c-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
