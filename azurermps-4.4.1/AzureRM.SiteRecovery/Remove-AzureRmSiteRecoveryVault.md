---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500689"
---
# <span data-ttu-id="030ad-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="030ad-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="030ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="030ad-102">SYNOPSIS</span></span>
<span data-ttu-id="030ad-103">Entfernt einen Standort Wiederherstellungs Tresor.</span><span class="sxs-lookup"><span data-stu-id="030ad-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="030ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="030ad-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="030ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="030ad-105">DESCRIPTION</span></span>
<span data-ttu-id="030ad-106">Das Cmdlet **Remove-AzureRmSiteRecoveryVault** löscht ein Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="030ad-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="030ad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="030ad-107">EXAMPLES</span></span>

## <span data-ttu-id="030ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="030ad-108">PARAMETERS</span></span>

### <span data-ttu-id="030ad-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="030ad-109">-Vault</span></span>
<span data-ttu-id="030ad-110">Gibt das Vault-Objekt der Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="030ad-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="030ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030ad-111">-DefaultProfile</span></span>
<span data-ttu-id="030ad-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="030ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="030ad-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030ad-113">CommonParameters</span></span>
<span data-ttu-id="030ad-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="030ad-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030ad-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="030ad-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030ad-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="030ad-116">INPUTS</span></span>

### <span data-ttu-id="030ad-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="030ad-117">ASRVault</span></span>
<span data-ttu-id="030ad-118">Der Parameter "Vault" akzeptiert den Wert vom Typ "ASRVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="030ad-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="030ad-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="030ad-119">OUTPUTS</span></span>

## <span data-ttu-id="030ad-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="030ad-120">NOTES</span></span>

## <span data-ttu-id="030ad-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="030ad-121">RELATED LINKS</span></span>

[<span data-ttu-id="030ad-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="030ad-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="030ad-123">Neu – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="030ad-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
