---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: b6016857054d2560602c7ea37a508317ff895d37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482709"
---
# <span data-ttu-id="cae56-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="cae56-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="cae56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cae56-102">SYNOPSIS</span></span>
<span data-ttu-id="cae56-103">Legt den Vault-Kontext für die Standortwiederherstellung für weitere Vorgänge fest.</span><span class="sxs-lookup"><span data-stu-id="cae56-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cae56-104">SYNTAX</span></span>

### <span data-ttu-id="cae56-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="cae56-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cae56-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="cae56-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cae56-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cae56-107">DESCRIPTION</span></span>
<span data-ttu-id="cae56-108">Das Cmdlet " **Set-AzureRmSiteRecoveryVaultSettings** " legt den Azure Site Recovery Vault-Kontext für weitere Vorgänge fest.</span><span class="sxs-lookup"><span data-stu-id="cae56-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="cae56-109">Dies gilt nicht für Vaults für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="cae56-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="cae56-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cae56-110">EXAMPLES</span></span>

## <span data-ttu-id="cae56-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cae56-111">PARAMETERS</span></span>

### <span data-ttu-id="cae56-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="cae56-112">-ARSVault</span></span>
<span data-ttu-id="cae56-113">Gibt ein **ARSVault** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cae56-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae56-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="cae56-114">-ASRVault</span></span>
<span data-ttu-id="cae56-115">Gibt ein **ASRVault** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cae56-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae56-116">-DefaultProfile</span></span>
<span data-ttu-id="cae56-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cae56-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae56-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae56-118">CommonParameters</span></span>
<span data-ttu-id="cae56-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae56-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae56-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae56-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae56-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cae56-121">INPUTS</span></span>

### <span data-ttu-id="cae56-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="cae56-122">ARSVault</span></span>
<span data-ttu-id="cae56-123">Der Parameter "ARSVault" akzeptiert den Wert vom Typ "ARSVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cae56-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="cae56-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="cae56-124">ASRVault</span></span>
<span data-ttu-id="cae56-125">Der Parameter "ASRVault" akzeptiert den Wert vom Typ "ASRVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cae56-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="cae56-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cae56-126">OUTPUTS</span></span>

### <span data-ttu-id="cae56-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="cae56-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="cae56-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="cae56-128">NOTES</span></span>

## <span data-ttu-id="cae56-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cae56-129">RELATED LINKS</span></span>

[<span data-ttu-id="cae56-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="cae56-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
