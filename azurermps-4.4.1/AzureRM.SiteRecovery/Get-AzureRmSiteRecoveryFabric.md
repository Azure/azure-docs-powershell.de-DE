---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481533"
---
# <span data-ttu-id="ff57b-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="ff57b-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="ff57b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff57b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff57b-103">Abrufen der Eigenschaften eines Azure Site Recovery-Fabrics</span><span class="sxs-lookup"><span data-stu-id="ff57b-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff57b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff57b-104">SYNTAX</span></span>

### <span data-ttu-id="ff57b-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff57b-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff57b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ff57b-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff57b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ff57b-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff57b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff57b-108">DESCRIPTION</span></span>
<span data-ttu-id="ff57b-109">Das Cmdlet " **Get-AzureRmSiteRecoveryFabric** " Ruft die Eigenschaften eines angegebenen Azure Site Recovery-Fabrics oder aller Azure Site Recovery-Fabrics in einem Recovery Service Vault ab.</span><span class="sxs-lookup"><span data-stu-id="ff57b-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="ff57b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff57b-110">EXAMPLES</span></span>

## <span data-ttu-id="ff57b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff57b-111">PARAMETERS</span></span>

### <span data-ttu-id="ff57b-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ff57b-112">-FriendlyName</span></span>
<span data-ttu-id="ff57b-113">Gibt den Anzeigenamen des Azure Site Recovery-Fabrics an.</span><span class="sxs-lookup"><span data-stu-id="ff57b-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff57b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ff57b-114">-Name</span></span>
<span data-ttu-id="ff57b-115">Gibt den Namen des Azure Site Recovery-Fabrics an.</span><span class="sxs-lookup"><span data-stu-id="ff57b-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff57b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff57b-116">-DefaultProfile</span></span>
<span data-ttu-id="ff57b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff57b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff57b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff57b-118">CommonParameters</span></span>
<span data-ttu-id="ff57b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff57b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff57b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff57b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff57b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff57b-121">INPUTS</span></span>

## <span data-ttu-id="ff57b-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff57b-122">OUTPUTS</span></span>

### <span data-ttu-id="ff57b-123">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ff57b-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ff57b-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff57b-124">NOTES</span></span>

## <span data-ttu-id="ff57b-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff57b-125">RELATED LINKS</span></span>

[<span data-ttu-id="ff57b-126">Neu – AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="ff57b-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="ff57b-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="ff57b-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
